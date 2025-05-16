# 🤖 Automated Resume Filtering Using UiPath

This project is an intelligent RPA solution developed using **UiPath** that automates the filtering and ranking of candidate resumes. The bot mimics the role of a recruiter by parsing PDF resumes, extracting relevant data, and scoring candidates based on job-specific requirements.

---

## 🚀 Key Features

- 🔍 Extracts key fields from resumes:
  - Full Name
  - Email
  - Skills
  - Degree
  - Experience (years)
- 📄 Supports both text-based and scanned (OCR) PDFs
- 📊 Matches resume content against:
  	- `job_title.txt`
- 📈 Scores candidates using this formula:
	- FinalScore = (SkillScore × 0.4) + (DegreeScore × 0.2) + (ExperienceScore × 0.4)

- 📝 Generates `CandidateScores.xlsx` with ranked candidates
- 💬 Detailed logs and fallback mechanisms handled in workflow

---

## 📁 Folder Structure
📁 Workflows/ → Contains UiPath project files (Main.xaml, project.json)
📁 Resumes/ → Input resumes in PDF format
📁 ReferenceFiles/ → Required skill list and job title
📁 Output/ → Final output Excel file with scores
📁 Demo/ → Demo video and screenshots
📁 Documentation/ → Project report, presentation files
📄 README.md → Project summary and usage
📄 .gitignore → Git exclusions for temp files

---

## 🧠 Technologies Used

- **UiPath Studio** – RPA platform for automation
- **Regex** – For custom field extraction
- **OCR** – For scanned PDF fallback (Tesseract or Google OCR)
- **Excel Automation** – To write and sort scored results
- **Markdown + Git** – For project versioning and documentation

---

## 🧪 How to Run the Bot

1. Open `Main.xaml` in **UiPath Studio**
2. Ensure the following folders are in place:
   - `Resumes/` → all input resumes (PDF)
   - `ReferenceFiles/` → contains `job_title.txt`
   - `Output/` → leave empty, bot will create Excel output here
3. Run the workflow
4. Check `Output/CandidateScores.xlsx` for sorted candidate rankings

---

## 📤 Output Example

After processing, the bot generates a file named `CandidateScores.xlsx` in the `Output/` folder. It contains the final ranked candidates with the following columns:

| Name            | Email             | currentTitle       | ExperienceYears | SkillMatchScore | DegreeScore | ExperienceScore | FinalScore |
|-----------------|-------------------|---------------------|------------------|------------------|--------------|------------------|-------------|
| Jade Nguyen     | jade.nguye@...    | Junior Business...  | 2                | 75               | 50           | 4                | **41.6**     |
| Jonas Keller    | jonas.kelle@...   | Data Analyst        | 6                | 75               | 30           | 12               | **40.8**     |
| Isabella Forbes | isabella.fo@...   | Senior Data Sc...   | 10               | 50               | 50           | 20               | **38.0**     |
| Julian Rivera   | julian.river@...  | Senior Data Sc...   | 10               | 75               | 0            | 20               | **38.0**     |
| ...             | ...               | ...                 | ...              | ...              | ...          | ...              | ...          |

> 💡 Candidates are ranked in descending order of **FinalScore**:

FinalScore = (SkillMatchScore × 0.4) + (DegreeScore × 0.2) + (ExperienceScore × 0.4)


> This score helps recruiters quickly shortlist the most qualified applicants.

---

## 🎥 Demo

📺 Watch the Resume Filtering Bot in action:  
[▶️ Watch Demo on YouTube](https://youtu.be/bmsUvxe0m1g)

---

## 📄 Documentation

- [📝 Final Report (PDF)](Documentation/FinalReport.pdf)
- [📊 Final Presentation Slides](Documentation/FinalPresentation.pptx)

---

## 🔮 Future Enhancements

- Integrate LinkedIn profile parsing
- Email shortlisted candidates directly via Outlook
- Deploy as unattended bot with Orchestrator
- Add Power BI dashboard for hiring trends

---

## 👨‍💻 Author

**Arsh Syed**  
Masters in Business Analytics with Data Science and AI  
🔍 Focused on building scalable, data-driven solutions across automation, machine learning, and artificial intelligence

---
