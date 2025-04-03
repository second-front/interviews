# Secure Artifact Manager Challenge

## Overview
Build a secure artifact storage and validation system that allows users to upload, scan, verify, and download binary artifacts with appropriate security guarantees. This challenge assesses your software engineering aptitude, security awareness, collaboration skills, and ability to deploy containerized applications in Kubernetes.

## Challenge Description
Create a web application that manages binary artifacts (like container images, packages, or executables). The system should track metadata, perform security scans, and provide secure access to these artifacts. Your solution must be containerized and deployable to a local Kubernetes cluster.

## Design Process: Request for Discussion (RFD)

Before implementation, you'll create an RFD document outlining your proposed solution. This follows our internal design process and serves as a framework for discussion with the review team.

Your RFD should:
1. Clearly define the problem and proposed solution
2. Document design decisions and tradeoffs
3. Outline architecture and implementation details
4. Address security considerations explicitly
5. Include Kubernetes deployment strategy and resource requirements
6. Serve as a discussion document with the review team

We've provided an RFD template in the `/challenges/templates/` directory. Submit your RFD as a pull request before beginning implementation. The review team will provide feedback, which you should incorporate before proceeding with development.

## Requirements by Level

### Level 1: Basic Functionality
- Frontend (React/TypeScript):
  - List/view artifacts with basic metadata
  - Upload and download functionality
  - Simple filtering and sorting
- Backend (Go or Rust):
  - REST API for artifact CRUD operations
  - Local filesystem storage
  - Basic user authentication
- Containerization:
  - Docker containers for frontend and backend
  - Multi-stage builds for optimized images
  - Docker Compose for local development

### Level 2: Security Enhancements
- Artifact metadata (size, upload time, SHA256 hash)
- Basic scanning for known vulnerabilities using an external tool
- User roles and permissions
- Audit logging of all actions
- Session management and secure authentication
- Kubernetes:
  - Basic Kubernetes manifest files (Deployments, Services)
  - ConfigMaps and Secrets for configuration
  - Resource limits and requests
  - Documentation of how to apply manifests manually

### Level 3: Advanced Features
- Artifact signing and verification
- Detailed vulnerability reports
- Artifact versioning and history
- Advanced filtering and search capabilities
- API key authentication option
- Kubernetes:
  - Fully functional deployment to local Kind cluster
  - Ingress configuration with TLS
  - Health checks and readiness probes
  - Persistent volume management for artifacts
  - Basic network policies
  - Deployment scripts or Helm charts

### Level 4: Enterprise Ready
- Integration with external scanning services
- Compliance reporting and attestations
- Approval workflows for artifact promotion
- Performance optimizations for large artifacts
- Comprehensive security controls
- Kubernetes:
  - GitOps-based deployment (ArgoCD or Flux)
  - Pod security policies or security contexts
  - Horizontal Pod Autoscaling
  - Custom admission controllers for security
  - Backup and disaster recovery strategy
  - Monitoring and alerting configuration

### Level 5: Extra Credit
- Implement one or more "surprise us" features that demonstrate your unique skills and understanding of the problem space
- Advanced Kubernetes features:
  - Custom Operators
  - Custom Resources Definitions (CRDs)
  - Service mesh integration
  - Multi-cluster deployment strategy
  - Advanced security implementations

## Technical Requirements
- Frontend: React with TypeScript
- Backend API: Go or Rust
- Containerization: Docker with multi-stage builds
- Orchestration: Kubernetes (aligned with your target level)
- Clean, well-tested code with appropriate error handling
- Security best practices throughout
- README with setup and usage instructions
- Complete RFD document submitted before implementation

## Kubernetes Requirements By Level

### Level 1
- Docker containers for all components
- Docker Compose for local development and testing
- No Kubernetes deployment required, but containerization must be production-ready

### Level 2
- Kubernetes manifest files for all components
- Documentation for manual deployment to a Kubernetes cluster
- Basic resource configuration and security considerations

### Level 3
- Deployment to a working Kind cluster with scripts or instructions
- Proper networking, storage, and security configuration
- Documentation for local cluster setup and deployment

### Level 4
- GitOps-based deployment pipeline
- Advanced Kubernetes security configurations
- Monitoring and observability setup
- Automated deployment process

## Common Pitfalls

We want to help you succeed in this challenge. Here are some common pitfalls to avoid:

1. **Scope Creep**: Many candidates try to implement too many features and run out of time. Focus on completing your chosen level well before adding extra features.

2. **Security as an Afterthought**: Security should be integrated from the beginning, not added at the end. Consider security implications in your initial design.

3. **Overcomplicating the Solution**: Keep your design as simple as possible while meeting the requirements. Eliminate unnecessary components and dependencies.

4. **Neglecting Error Handling**: Proper error handling is essential, especially in security-critical applications. Make sure errors are caught, logged, and handled appropriately.

5. **Poor Documentation**: Your solution should be well-documented, including setup instructions, API documentation, and security considerations.

6. **Code Structure**: Avoid leaving commented-out code chunks or creating monolithic files. Organize your code with clear separation of concerns.

7. **Ignoring Containerization Best Practices**: Don't create unnecessarily large containers or ignore security hardening measures. Follow container best practices.

8. **Kubernetes Complexity**: Match your Kubernetes implementation to your experience level. It's better to have a well-executed Level 2 solution than a problematic Level 4 solution.

9. **Communication Gaps**: Regular updates in Slack and thoughtful questions demonstrate your collaboration skills. Don't go silent for extended periods.

10. **Underestimating the RFD**: The RFD is a critical part of the challenge. Invest appropriate time in creating a thoughtful, well-structured design document.

## Questions

We encourage you to ask questions throughout the challenge. Here are guidelines for effective communication:

### Good Questions to Ask:
- Clarifying questions about functional requirements: "Should artifact versioning support semantic versioning or is any versioning scheme acceptable?"
- Security approach questions: "What level of vulnerability scanning is expected at Level 2? Is integration with a specific scanner required?"
- Deployment clarifications: "For Level 3, should the Kind cluster support multiple nodes or is a single-node cluster sufficient?"

### Implementation Decisions You Should Make:
- Choice of specific technologies within the required frameworks
- Architecture and design patterns within your code
- Testing frameworks and approaches
- Specific UI/UX design decisions
- Container optimization techniques

Remember, we're evaluating both your technical skills and your ability to communicate effectively. Don't hesitate to ask thoughtful questions, but also demonstrate independent problem-solving for implementation-specific details.

## Evaluation Criteria
- RFD quality and completeness
- Code quality and organization
- Security implementation and awareness
- Kubernetes deployment architecture and practices (appropriate to your level)
- Testing approach and coverage
- Documentation quality
- Collaboration with the review team
- Questions asked during development

## Process
1. Fork the provided repository
2. Create and submit an RFD within 3 days
3. Discuss and refine the RFD with the review team
4. Implement the solution (target completion: 2 weeks)
5. Regular commits showing incremental progress
6. Ask questions in the provided Slack channel

## Collaboration
You'll interact with 2-3 team members throughout the challenge. They will review your RFD, answer questions, and provide feedback. Effective communication in this process is part of the evaluation.