# Create New Agent

> **Type**: Task
> **Category**: operations
> **Agents**: Traffic Chief
> **Frameworks**: Agent Design Framework, Role Definition Protocol
> **Checklists**: new-agent-checklist
> **Output template**: templates/agent-definition.md

## ROUTING

> **Agents**: traffic-chief, ads-analyst
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Design and create a new agent for the Traffic Masters Squad by defining its role, expertise domain, decision authority, interaction patterns, and integration with existing squad workflows.

## Inputs
- Identified capability gap in the current squad
- Role requirements: what the agent needs to do that no current agent covers
- Existing agent roster with roles and responsibilities
- Squad workflow documentation showing where the new agent fits
- Reference materials for the agent's expertise domain
- Naming conventions and agent definition templates

## Steps
1. Document the capability gap: what tasks are underserved by current agents
2. Define the agent's primary role and expertise domain with clear boundaries
3. Name the agent following squad naming conventions and domain alignment
4. Write the agent's persona: expertise background, perspective, and decision-making style
5. Define the agent's responsibilities: specific tasks and workflows it owns
6. Specify decision authority: what the agent can decide independently vs requires escalation
7. Map interaction patterns: which agents it collaborates with and on what topics
8. Define the agent's frameworks and methodologies it applies
9. Specify the checklists the agent uses and contributes to
10. Write example prompts and responses to calibrate the agent's behavior
11. Integrate the agent into existing workflows: update task assignments and review processes
12. Test the agent definition by running it through a representative task

## Output
Agent definition document containing: role description, expertise domain, persona, responsibilities, decision authority, interaction map, frameworks, checklists, example behaviors, and workflow integration notes.

## Quality Gate
- New agent checklist confirms all definition elements completed
- Agent does not overlap significantly with existing agent responsibilities
- Traffic Chief validates the agent fills the identified capability gap

## Duration
2-4 hours for definition and design; 1-2 hours for testing and refinement
