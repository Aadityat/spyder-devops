<h1>🚀 DevOps Spyder – CI/CD Pipeline Project</h1>

<h2>📌 Project Overview</h2>
<p>
<strong>DevOps Spyder</strong> is a full-stack DevOps project that demonstrates how a modern application is
<b>built, containerized, and deployed automatically</b> using industry-standard tools and practices.
</p>
<p>
The project focuses on <b>CI/CD automation</b>, <b>container-based architecture</b>, and
<b>cloud deployment</b> using a clean and reproducible workflow.
</p>

<hr>

<h2>🧱 Tech Stack</h2>
<table>
  <tr><th align="left">Category</th><th align="left">Tools</th></tr>
  <tr><td>Version Control</td><td>Git, GitHub</td></tr>
  <tr><td>CI/CD</td><td>GitHub Actions</td></tr>
  <tr><td>Containerization</td><td>Docker, Docker Compose</td></tr>
  <tr><td>Container Registry</td><td>GitHub Container Registry (GHCR)</td></tr>
  <tr><td>Cloud</td><td>AWS EC2</td></tr>
  <tr><td>Reverse Proxy</td><td>Nginx</td></tr>
  <tr><td>Frontend</td><td>React</td></tr>
  <tr><td>Backend</td><td>Node.js</td></tr>
</table>

<hr>

<h2>🗂️ Project Structure</h2>

<pre>
.
├── Frontend/             # React frontend service
│   └── Dockerfile
├── Backend/              # Node.js backend API
│   └── Dockerfile
├── nginx/                # Reverse proxy layer
│   └── nginx.conf
├── .github/
│   └── workflows/
│       └── ci-cd.yml     # GitHub Actions pipeline
├── docker-compose.local.yml
├── docker-compose.prod.yml
├── .dockerignore
├── .gitignore
└── README.md
</pre>

<hr>

<h2>⚙️ System Architecture Flow</h2>
<ol>
  <li>Code is pushed to <b>GitHub</b></li>
  <li><b>GitHub Actions</b> CI/CD pipeline is triggered</li>
  <li>Docker images are built for frontend, backend, and Nginx</li>
  <li>Images are pushed to <b>GitHub Container Registry (GHCR)</b></li>
  <li>AWS EC2 pulls images from GHCR</li>
  <li>Services are started using <b>Docker Compose</b></li>
  <li>Nginx routes traffic between frontend and backend</li>
</ol>

<hr>

<h2>🔁 CI/CD Pipeline</h2>
<ul>
  <li>Implemented using <b>GitHub Actions</b></li>
  <li>Handles source code checkout, Docker image build, and push to GHCR</li>
  <li>Provides automated and repeatable deployments</li>
</ul>

<hr>

<h2>🐳 Docker &amp; Docker Compose</h2>
<ul>
  <li>Each service runs in its own container</li>
  <li>Docker Compose manages multi-container orchestration and networking</li>
  <li>Ensures consistent behavior across environments</li>
</ul>

<hr>

<h2>🌐 Nginx in the Architecture</h2>
<p>
Nginx acts as a <b>reverse proxy</b> and single entry point for the application.
</p>
<ul>
  <li>Routes <code>/</code> requests to the frontend service</li>
  <li>Routes <code>/api</code> requests to the backend service</li>
  <li>Decouples frontend and backend services</li>
  <li>Improves maintainability and scalability</li>
</ul>

<hr>

<h2>🧩 Architecture Files</h2>

<h3>.gitignore</h3>
<ul>
  <li>Prevents committing unnecessary or sensitive files</li>
  <li>Excludes dependencies, logs, environment files, and build artifacts</li>
</ul>

<h3>.dockerignore</h3>
<ul>
  <li>Defined at the repository root</li>
  <li>Excludes unnecessary files from Docker build context</li>
  <li>Improves build speed and reduces image size</li>
</ul>

<hr>

<h2>🔐 Versioning &amp; Rollback (Brief)</h2>
<ul>
  <li>Docker images are tagged during the CI pipeline</li>
  <li>Once pulled, images remain available on the EC2 instance</li>
  <li>A previous image can be redeployed by restarting containers using Docker Compose</li>
</ul>

<hr>

<h2>☁️ Deployment Environment</h2>
<ul>
  <li>Application is deployed on <b>AWS EC2</b></li>
  <li>Docker and Docker Compose are used for execution</li>
  <li>Images are pulled from GHCR during deployment</li>
  <li>No manual code transfer to the server</li>
</ul>

<hr>

<h2>🎯 DevOps Concepts Demonstrated</h2>
<ul>
  <li>Automated CI/CD pipelines</li>
  <li>Containerized application architecture</li>
  <li>Reverse proxy-based routing</li>
  <li>Cloud deployment using Docker</li>
  <li>Basic rollback awareness</li>
</ul>

<hr>

<h2>👤 Author</h2>
<p>
<b>Aditya Tiwari</b><br>
DevOps &amp; Cloud Enthusiast<br>
MCA – NIT Trichy
</p>

<hr>
