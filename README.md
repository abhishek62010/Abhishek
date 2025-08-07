# Abhishek
My Portfolio
from reportlab.platypus import SimpleDocTemplate, Paragraph, Spacer, Image
from reportlab.lib.styles import getSampleStyleSheet, ParagraphStyle
from reportlab.lib.pagesizes import A4
from reportlab.lib.enums import TA_CENTER
from reportlab.lib.units import inch

# Set up the PDF document
pdf_path = "/mnt/data/Abhishek_GitHub_Readme_Portfolio.pdf"
doc = SimpleDocTemplate(pdf_path, pagesize=A4)
styles = getSampleStyleSheet()
style_normal = styles["Normal"]
style_heading = ParagraphStyle("Heading", parent=styles["Heading1"], alignment=TA_CENTER, fontSize=18, spaceAfter=14)
style_subheading = ParagraphStyle("SubHeading", parent=styles["Heading2"], spaceAfter=8)
style_code = ParagraphStyle("Code", parent=styles["Code"], fontName='Courier', fontSize=9, spaceAfter=6)

# Content blocks
content = []

content.append(Paragraph("Hi 👋, I'm Abhishek Kumar", style_heading))
content.append(Paragraph("🔍 Data Analyst | Python | SQL | Power BI | Excel | Visualization | AI Enthusiast", style_normal))
content.append(Spacer(1, 12))

content.append(Paragraph("🧑‍💻 About Me", style_subheading))
content.append(Paragraph("""
🎓 BCA Graduate from CIMAGE College, Patna (Aryabhatta Knowledge University)<br/>
🧠 Data enthusiast with solid skills in Python, SQL, Power BI, and Excel<br/>
📊 Passionate about extracting insights from data & creating dashboards<br/>
💼 Completed virtual internships with JP Morgan, Accenture<br/>
🏆 Certified in Python, JavaScript, Java, Big Data, Excel, and more<br/>
✨ Exploring AI tools like ChatGPT & DeepSeek<br/>
📬 Reach me at: Abhishekkr62010@gmail.com
""", style_normal))
content.append(Spacer(1, 12))

content.append(Paragraph("💼 Featured Projects", style_subheading))
content.append(Paragraph("""
📈 Stock Price Data Interface - JP Morgan (Virtual) - Python, API, Data Parsing<br/>
🔐 Cybersecurity Defense Simulation - JP Morgan (Virtual) - Network Security, Logs<br/>
📊 Data Analytics Dashboard - Accenture (Virtual) - Excel, Power BI, Visualization
""", style_normal))
content.append(Spacer(1, 12))

content.append(Paragraph("🛠️ Tech Stack & Skills", style_subheading))
content.append(Paragraph("""
Languages: Python, SQL, JavaScript, Java, HTML, CSS<br/>
Data Tools: Power BI, Excel, Pandas, NumPy<br/>
Web Development: HTML, CSS, JavaScript (Basic)<br/>
Databases: MySQL<br/>
Tools & Platforms: Git, GitHub, VS Code, ChatGPT, DeepSeek<br/>
Concepts: Data Structures, Cybersecurity, Cloud Computing, SDLC
""", style_normal))
content.append(Spacer(1, 12))

content.append(Paragraph("🎓 Certifications", style_subheading))
content.append(Paragraph("""
🐍 Python Programming – Great Learning, IIT Bombay<br/>
☕ Java & JavaScript – IIT Bombay Spoken Tutorial<br/>
🧠 AI Engineer, Data Analyst, Excel – One Roadmap<br/>
📊 Discover Data Analysis – Microsoft Learn<br/>
🖥️ Big Data & Hadoop – CIMAGE College
""", style_normal))
content.append(Spacer(1, 12))

content.append(Paragraph("🏅 Achievements", style_subheading))
content.append(Paragraph("""
✅ Certified Developer – IIT Bombay Spoken Tutorial<br/>
🌍 Completed virtual internships from global companies<br/>
💬 Fluent in English and Hindi<br/>
💡 Strong in problem-solving, analytical thinking, and team collaboration
""", style_normal))
content.append(Spacer(1, 12))

content.append(Paragraph("📫 Connect With Me", style_subheading))
content.append(Paragraph("""
🔗 LinkedIn: https://www.linkedin.com/in/your-profile<br/>
📧 Email: Abhishekkr62010@gmail.com<br/>
💻 GitHub: https://github.com/abhikumar62010
""", style_normal))

# Build the PDF
doc.build(content)
pdf_path
