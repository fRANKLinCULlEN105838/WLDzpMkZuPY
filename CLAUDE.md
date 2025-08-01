# AutoBE Project Context for Claude

## Project Overview
AutoBE is an AI-powered no-code agent that automatically generates complete backend applications using TypeScript, NestJS, and Prisma. The system follows a waterfall development model with compiler feedback validation to ensure 100% working code output.

## Core Architecture
The system consists of specialized agents working in sequence:

### Functional Agents
- **Analyze Agent**: Requirements analysis and specifications
- **Prisma Agent**: Database schema design (ERD) with Postgres/SQLite support
- **Interface Agent**: API design and OpenAPI specification generation
- **Test Agent**: End-to-end test code generation with scenario planning
- **Realize Agent**: Main program implementation and integration

### Compiler Validation
- Prisma Compiler: Validates database schemas
- OpenAPI Validator: Validates API specifications  
- TypeScript Compiler: Validates generated code quality

## Project Structure
```
/autobe/
   assets/                    # Compiler dependencies and repositories
   deploy/                    # Deployment scripts
   internals/                 # Internal configurations and dependencies
   packages/                  # Core package modules
   test/                      # Comprehensive test suite and results
   website/                   # Documentation website (Next.js)
   playground/                # Interactive demo environment
   CLAUDE.md                  # This file
```

## Key Technologies
- **Backend Stack**: TypeScript + NestJS + Prisma
- **Database**: PostgreSQL (primary), SQLite (development)
- **API**: OpenAPI/Swagger specification
- **Testing**: Automated e2e test generation
- **Validation**: Multi-layer compiler feedback

## Development Phase
Currently in **Beta Phase** (2025-06-01 to 2025-08-31) focusing on:
- Test Agent refinement with compiler feedback
- Realize Agent development with runtime validation
- 100% autonomous backend development capability
- Ecosystem integration preparation

## Ecosystem Vision
Part of WrtnLabs' no-code ecosystem:
- **@autobe**: Backend application generation
- **@agentica**: AI chatbot creation from swagger.json
- **@autoview**: Frontend application generation from swagger.json

Mission: "Can you converse? Then you're a full-stack developer."

## Example Use Cases
1. **BBS (Bulletin Board System)**: Political/economic discussion platform
2. **E-Commerce Platform**: Shopping mall with voice-driven interactions
3. **Custom Business Applications**: Requirement-driven development

## Key Features
- **Waterfall Model**: Systematic phase-by-phase development
- **Compiler Feedback**: Real-time validation and error correction
- **Function Calling**: AI agent coordination and task distribution
- **WebSocket Support**: Real-time communication protocols
- **Schema-First Development**: Database-driven architecture

## Testing & Validation
- Automated test scenario generation
- Compiler-validated code output
- Benchmark performance testing
- End-to-end integration testing

## Instructions for Claude

### Communication Language
- **Write all code, comments, and documentation in English**
- **Communicate with the user in Korean (\m�)**
- Maintain professional yet conversational tone in Korean

### Development Guidelines
1. Follow the existing TypeScript/NestJS/Prisma patterns
2. Respect the waterfall development sequence when making changes
3. Ensure compiler validation passes for any generated code
4. Reference the test results in `/test/results/` for examples
5. Use the existing agent patterns found in `/packages/` directory

### Project Context Awareness
- This is a production-ready no-code agent system
- Code quality must be enterprise-grade
- All generated code should follow the established patterns
- Consider the multi-agent architecture when suggesting changes
- Be aware of the compiler feedback loop integration

### Useful Commands
- `pnpm build`: Build all packages
- `pnpm playground`: Run interactive demo
- `pnpm test`: Run test suite
- Check `/test/scripts/` for specific testing scenarios

### Repository Information
- **License**: MIT
- **Maintainer**: Wrtn Technologies
- **Repository**: https://github.com/wrtnlabs/autobe
- **Documentation**: https://wrtnlabs.io/autobe/docs/
- **Main Branch**: main