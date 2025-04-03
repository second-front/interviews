# Candidate Guide: Secure Artifact Manager Challenge

## Introduction
Welcome to the Secure Artifact Manager challenge! This guide will help you navigate the exercise successfully. We're excited to see your approach to building secure, well-designed software that runs in containers and Kubernetes.

## Getting Started

### Timeline
- RFD Creation and Submission: Within 3 days of receiving the challenge
- RFD Discussion and Refinement: 2-3 days
- Implementation Period: Up to 2 weeks
- Code Review: After submission

### Repository Setup
1. Fork the provided repository
2. Clone your fork locally
3. Create a branch for your work
4. Follow the standard git workflow (regular commits, descriptive messages)

## The RFD Process

### What is an RFD?
An RFD (Request for Discussion) is a design document that outlines your proposed solution before implementation. It serves as both a planning tool and a discussion framework. We use RFDs internally to document design decisions and facilitate collaborative engineering.

### Creating Your RFD
1. Use the provided template in `/challenges/templates/rfd-template.md`
2. Assign your RFD an identifier (e.g., "RFD 0001")
3. Complete each section of the template with your proposed design
4. Set the initial status to "prediscussion"

### RFD Lifecycle
1. **Prediscussion**: Initial creation of your RFD
2. **Discussion**: Submit your RFD as a PR for review and feedback
3. **Published**: RFD is approved and implementation can begin

### RFD Best Practices
- Be concise but thorough
- Explain the reasoning behind design decisions
- Document trade-offs and alternatives considered
- Include diagrams where helpful
- Address security implications explicitly
- Detail your containerization and Kubernetes strategy appropriate to your target level
- Ask specific questions where you need input

## Implementation Guidelines

### Technical Requirements
- Frontend: React with TypeScript
  - Clean component architecture
  - Type safety
  - Responsive design
- Backend: Go or Rust
  - RESTful API design
  - Clean separation of concerns
  - Proper error handling
- Containerization:
  - Multi-stage Docker builds
  - Minimal container images
  - Security considerations (non-root users, etc.)
- Kubernetes (scaled by level, see below)
- Documentation
  - Clear README with setup instructions
  - API documentation
  - Deployment instructions

### Containerization and Kubernetes Guidelines by Level

#### Level 1: Containerization
- Create proper Dockerfiles for all components
- Use multi-stage builds to minimize image size
- Implement Docker Compose for local development
- Consider security in your container builds
- No Kubernetes deployment required at this level

#### Level 2: Kubernetes Manifests
- Create basic Kubernetes manifests (Deployments, Services, etc.)
- Configure environment variables using ConfigMaps and Secrets
- Set appropriate resource requests and limits
- Document how to apply these manifests manually
- No automated deployment required at this level

#### Level 3: Kind Cluster Deployment
- Provide scripts or instructions for setting up a local Kind cluster
- Ensure your application deploys and runs correctly in Kind
- Configure proper networking, including ingress if needed
- Set up persistent storage for artifacts
- Implement basic network policies and security measures
- Use Helm charts or deployment scripts for easier installation

#### Level 4: GitOps and Advanced K8s
- Implement GitOps-based deployment using tools like ArgoCD or Flux
- Configure advanced security measures
- Set up monitoring and observability
- Implement autoscaling and high-availability features
- Document your GitOps workflow and practices

### Level Selection
While the challenge has 5 levels, aim to complete at least Level 2. A complete Level 2 implementation is better than a partial Level 4 implementation. Focus on quality over quantity.

### Testing
Include tests for your code:
- Unit tests for core business logic
- Integration tests for key workflows
- Container tests (e.g., testing Docker images)
- Kubernetes deployment tests (for Level 3+)

## Avoiding Common Pitfalls

Review the "Common Pitfalls" section in the challenge description carefully. Here are some additional tips:

1. **Start Simple**: Begin with a minimally viable solution that meets the core requirements, then iterate.

2. **Plan Your Time**: Allocate time for each phase - RFD creation, implementation, testing, and documentation.

3. **Security-First Mindset**: Consider security implications at every step, not just as a final check.

4. **Consistent Communication**: Regular updates show your engagement and provide opportunities for feedback.

5. **Focus on Completion**: It's better to complete a lower level thoroughly than to partially complete a higher level.

6. **Test Continuously**: Don't leave testing until the end. Write tests as you implement features.

7. **Document As You Go**: Keep documentation updated throughout development, not just at the end.

## Asking Good Questions

The "Questions" section in the challenge description provides guidelines on what types of questions are appropriate. Remember:

- Ask clarifying questions about requirements or expectations
- Demonstrate thoughtfulness in your questions
- Be specific rather than general
- Show that you've already considered possible solutions
- Balance questions with independent problem-solving

## Collaboration

### Using the Slack Channel
- Introduce yourself when you start
- Ask specific, well-formed questions
- Share your RFD for feedback
- Provide regular progress updates (2-3 times per week)

### RFD Review Process
After submitting your RFD:
1. The review team will provide comments and questions
2. You should address feedback and update your RFD
3. Once approved, you can begin implementation

### Code Review Process
After submission, team members will:
1. Review your code and deployment configuration
2. Provide written feedback
3. Schedule a review call to discuss your solution

## Evaluation Focus

We're particularly interested in:
- RFD quality and thoroughness
- Your problem-solving approach
- Security implementation and awareness
- Code quality and organization
- Containerization and Kubernetes implementation (appropriate to your level)
- Testing strategy
- Communication and collaboration
- How you incorporate feedback

## Final Checklist Before Submission
- Completed implementation meeting your target level requirements
- All tests passing
- Documentation complete
- Code is clean and well-organized
- Container images build successfully
- Kubernetes deployment works as expected (if applicable to your level)
- No security vulnerabilities in dependencies
- RFD updated to reflect the final implementation

Good luck! We look forward to seeing your solution.