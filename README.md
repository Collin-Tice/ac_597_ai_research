# ac_597_ai_research
Work related to the pilot AI course at the University of Alabama

test 1- creating a personal resume website using vibe coding
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Collin Tice</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #f4f6f8;
        }

        /* ===== Top Banner ===== */
        header {
            background-color: #1f2933;
            color: white;
            padding: 15px 30px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .site-name {
            font-size: 22px;
            font-weight: bold;
        }

        nav button {
            background: none;
            border: none;
            color: white;
            font-size: 16px;
            margin-left: 20px;
            cursor: pointer;
        }

        nav button:hover {
            text-decoration: underline;
        }

        /* ===== Page Layout ===== */
        .container {
            padding: 30px;
        }

        .section {
            display: none;
        }

        .section.active {
            display: block;
        }

        h2 {
            margin-top: 0;
        }

        /* ===== Boxes ===== */
        .box {
            background-color: white;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 6px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        textarea, input[type="text"] {
            width: 100%;
            padding: 10px;
            margin-top: 10px;
            border-radius: 4px;
            border: 1px solid #ccc;
            resize: vertical;
        }

        /* ===== Home Page Layout ===== */
        .home-grid {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 20px;
        }

        .right-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        /* ===== Headshot ===== */
        .headshot {
            text-align: center;
        }

        .headshot input {
            margin-top: 10px;
        }

        /* ===== Add More Button ===== */
        .add-btn {
            margin-top: 10px;
            padding: 8px 12px;
            background-color: #1f2933;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        .add-btn:hover {
            background-color: #374151;
        }
    </style>
</head>

<body>

<header>
    <div class="site-name">Collin Tice</div>
    <nav>
        <button onclick="showSection('home')">Home</button>
        <button onclick="showSection('education')">Education</button>
        <button onclick="showSection('work')">Work Experience</button>
        <button onclick="showSection('projects')">Projects and Awards</button>
    </nav>
</header>

<div class="container">

    <!-- ===== HOME ===== -->
    <div id="home" class="section active">
        <div class="home-grid">
            
            <div class="box headshot">
                <h3>Professional Headshot</h3>
                <p>Upload your headshot here</p>
                <input type="file" accept="image/*">
            </div>

            <div>
                <div class="box">
                    <h3>Professional Summary</h3>
                    <textarea rows="6" placeholder="Write a summary about yourself..."></textarea>
                </div>

                <div class="right-grid">
                    <div class="box">
                        <h3>Skills</h3>
                        <textarea rows="6" placeholder="List your skills..."></textarea>
                    </div>

                    <div class="box">
                        <h3>Links</h3>
                        <textarea rows="6" placeholder="Paste LinkedIn, GitHub, or other links..."></textarea>
                    </div>
                </div>
            </div>

        </div>
    </div>

    <!-- ===== EDUCATION ===== -->
    <div id="education" class="section">
        <div class="box">
            <h2>Education</h2>
            <div id="education-list">
                <textarea rows="4" placeholder="Add education details..."></textarea>
            </div>
            <button class="add-btn" onclick="addField('education-list')">Add More</button>
        </div>

        <div class="box">
            <h2>Certifications</h2>
            <textarea rows="4" placeholder="Add certifications..."></textarea>
        </div>
    </div>

    <!-- ===== WORK EXPERIENCE ===== -->
    <div id="work" class="section">
        <div class="box">
            <h2>Work Experience</h2>
            <div id="work-list">
                <textarea rows="4" placeholder="Add work experience..."></textarea>
            </div>
            <button class="add-btn" onclick="addField('work-list')">Add More</button>
        </div>
    </div>

    <!-- ===== PROJECTS & AWARDS ===== -->
    <div id="projects" class="section">
        <div class="box">
            <h2>Projects</h2>
            <textarea rows="6" placeholder="Paste project descriptions or links..."></textarea>
        </div>

        <div class="box">
            <h2>Awards</h2>
            <textarea rows="6" placeholder="List awards..."></textarea>
        </div>
    </div>

</div>

<script>
    function showSection(id) {
        document.querySelectorAll('.section').forEach(section => {
            section.classList.remove('active');
        });
        document.getElementById(id).classList.add('active');
    }

    function addField(containerId) {
        const container = document.getElementById(containerId);
        const textarea = document.createElement("textarea");
        textarea.rows = 4;
        textarea.placeholder = "Add more details...";
        container.appendChild(textarea);
    }
</script>

</body>
</html>
