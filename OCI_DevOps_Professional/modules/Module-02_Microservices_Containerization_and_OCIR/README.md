# 📘 Microservices Module

## 1️⃣ Trainer's Lesson Notes

### What are Microservices?

* **Architecture style** → breaks applications into small, independent services
* Each service has:
   * its own codebase
   * lifecycle
   * team ownership
* Services communicate via **APIs** (REST, gRPC, event streaming)

### Monolithic vs Microservices

#### Monolithic:
* Single codebase & deployment
* Tightly coupled modules
* Harder to scale (must scale entire app)

#### Microservices:
* Independent services
* Each service deployable separately
* Easier to scale specific parts of the system
* Fault isolation (failure in one doesn't kill whole app)

### Benefits of Microservices

* **Agility** → Faster, independent development
* **Scalability** → Scale services independently
* **Resilience** → Fault isolation & recovery
* **Faster Deployment** → Continuous delivery per service
* **Technology Freedom** → Each team chooses its tech stack
* **Improved DevOps adoption** → Encourages CI/CD culture

### Challenges of Microservices

* **Complexity** → More moving parts
* **Data management** → Each service may need its own DB
* **Network communication** → More inter-service calls
* **Monitoring & Debugging** → Harder than monoliths
* **Security** → Must secure APIs between services

### Microservices in DevOps

* Microservices + Containers = Perfect match
* Containers provide **isolation + portability** for each service
* Kubernetes (OKE in OCI) orchestrates microservices at scale
* CI/CD pipelines handle automated build → test → deploy per service

---

# 📘 Containers and Docker Module

## 1️⃣ Trainer's Lesson Notes

### Benefits of Containerization

* **Portability** – Run apps across environments without modification
* **Agility** – Faster updates and deployments
* **Speed** – Rapid provisioning and scaling
* **Fault Isolation** – Containers isolate failures
* **Efficiency** – Lightweight compared to VMs
* **Ease of Management** – Unified workflows
* **Security** – Controlled and sandboxed runtime

### Docker Components

* **Docker Client** → Commands like `docker build`, `docker run`, `docker pull`
* **Daemon** → Manages containers/images via REST API
* **Images** → Templates (e.g., PostgreSQL, Node, Python)
* **Containers** → Running instances of images
* **Volumes** → Persistent storage
* **Docker Registry** → Central repository (e.g., DockerHub, OCIR)

### VMs vs Containers

* **VMs** → Each VM has its own OS + binaries. Heavy
* **Containers** → Share host OS kernel, lightweight, start quickly

### Basic Docker Commands (Containers)

* `docker run [IMAGE_NAME]` → Run container
* `docker start|stop|restart [CONTAINER]` → Manage lifecycle
* `docker ps` → List containers
* `docker logs [CONTAINER]` → Logs
* `docker rm [CONTAINER]` → Remove

### Dockerfile

* **FROM** → Base image
* **RUN** → Execute commands
* **WORKDIR** → Set working directory
* **COPY** → Copy files
* **ENV** → Environment variables
* **EXPOSE** → Ports
* **CMD / ENTRYPOINT** → Default execution command
* **LABEL** → Metadata

### Basic Docker Commands (Images)

* `docker image pull` → Download image
* `docker build` → Build from Dockerfile
* `docker commit` → Save container as image
* `docker tag` → Tag image
* `docker push` → Upload to registry
* `docker image ls` → List images
* `docker rmi` → Remove image

### Oracle Cloud Infrastructure Registry (OCIR)

* **Managed container registry** in OCI
* Stores & manages container images
* Supports **push/pull** via CLI
* OCI-compliant (Open Container Initiative)
* Supports Helm charts & multi-architecture images
* Integrates with OCI VCN for private access

**Key Benefits:** Integration, Security, Regional Availability, High Availability, Anywhere Access, Repo Quotas

### Container Registry Concepts

* **Image** → Template with dependencies
* **Repository** → Collection of images (different versions)
* **Registry** → Stores repos, accessible globally

### OCIR Terminology

* **Region Key** → e.g., `iad.ocir.io`, `us-phoenix-1.ocir.io`
* **Tenancy Namespace** → Unique to your tenancy
* **Repo Name** → Logical project name (`project01/acme-web-app`)
* **Image Name & Tag** → e.g., `acme-web-app:4.6.3`
* **Image Path** → `<region>.ocir.io/<namespace>/<repo>:<tag>`

### Managing Images in OCIR

* View image details
* Push/pull via Docker CLI
* Delete/undelete images
* Use retention policies
* Untag images
* Pull during Kubernetes deployments with `kubectl` secrets

## 2️⃣ Exam & Interview Notes

* **Containers vs VMs** → Containers share host kernel; VMs are heavier
* **Dockerfile** → Core commands (`FROM`, `RUN`, `COPY`, `CMD`, etc.)
* **CI/CD pipelines** → Containerization simplifies portability across environments
* **OCIR** → Oracle-managed registry (push/pull, Helm, multi-arch)

### Key Terminology:
* **Registry Identifier** → `<region>.ocir.io/<namespace>`
* **Image Path** → Full reference to push/pull

**Pitfall:** Mixing up **repository** vs **registry**

## 3️⃣ Beyond Certification (DevOps Engineer View)

* **Docker in DevOps:** Used for consistent app packaging in CI/CD pipelines
* **OCI DevOps Integration:** OCIR works with OCI DevOps pipelines → push built images, deploy to OKE

### Real-world mapping:
* Local build (`docker build`) → Push to OCIR → Deployment on Kubernetes (OKE)
* Observability with Prometheus/Grafana → tie container metrics with OCI Monitoring
