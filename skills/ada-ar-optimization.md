---
name: ada-ar-optimization
description: Analyze automated resolution rate and get recommendations for improving AR using Ada's AI agent data. Use when the user asks about improving automation, reducing handoffs, increasing resolution rate, or understanding why conversations aren't being resolved automatically.
license: Apache-2.0
compatibility: Requires Ada MCP server connected to Claude Desktop or compatible MCP client
metadata:
  author: ada
  version: "1.0"
allowed-tools: get_ada_metric get_available_filters get_conversations_by_filters get_conversation get_ada_configuration search_knowledge search_coaching
---

# Improving Automated Resolution Rate with Ada

## When to use this skill

Use this skill when the user wants to:
- Improve their automated resolution (AR) rate
- Reduce handoffs to human agents
- Understand why conversations aren't being resolved automatically
- Identify automation opportunities
- Analyze unresolved conversation patterns

## Understanding AR

Automated Resolution (AR) measures the percentage of conversations fully resolved by the AI agent without human intervention. Key factors affecting AR:

- **Knowledge coverage**: Does the agent have answers to customer questions?
- **Action capabilities**: Can the agent perform the required tasks?
- **Playbook design**: Are workflows comprehensive enough?
- **Handoff triggers**: Are handoffs happening unnecessarily?

## Workflow

### Step 1: Get current AR metrics

Establish the baseline:

```
Use get_ada_metric to retrieve:
- Automated resolution rate (last 7 days and last 30 days for trend)
- Engaged conversation volume
```

Calculate week-over-week or month-over-month changes if data is available.

### Step 2: Identify unresolved conversations

Find where automation is failing:

```
1. Use get_available_filters to understand filter options
2. Use get_conversations_by_filters with automated_resolution_status = "Unresolved"
3. Request 50-100 conversations for pattern analysis
```

### Step 3: Analyze resolution reasons

Examine why conversations weren't resolved:

```
Use get_conversation on 15-25 unresolved conversations
```

Categorize by failure reason:
- **Knowledge gap**: Agent didn't have the answer
- **Action limitation**: Agent couldn't perform the required task
- **Handoff trigger**: Explicit handoff request or rule triggered
- **Complexity**: Multi-step issue beyond current capabilities
- **Edge case**: Unusual scenario not covered by playbooks

### Step 4: Identify high-volume failure patterns

Look for the biggest opportunities:

```
Review customer_inquiry_summary and automated_resolution_reason fields
```

Group by:
- Topic/intent
- Failure reason
- Volume (how many conversations with this pattern?)

### Step 5: Review current configuration

Understand existing capabilities:

```
Use get_ada_configuration to retrieve:
- Playbooks (what workflows exist?)
- Actions (what can the agent do?)
- Coaching (what guidance exists?)
- Knowledge (through search_knowledge for specific topics)
```

### Step 6: Search for coverage gaps

For each high-volume failure pattern:

```
1. Use search_knowledge to check if relevant articles exist
2. Use search_coaching to check for relevant guidance
```

### Step 7: Provide prioritized recommendations

Structure by impact and effort:

```markdown
## High Impact, Low Effort
- Quick knowledge additions
- New coaching rules
- Playbook tweaks

## High Impact, High Effort  
- New action integrations
- Complex playbook creation
- API connections

## Medium Impact
- Edge case coverage
- Refinements to existing content
```

## Example output format

```markdown
## AR Analysis Summary

**Current AR**: 65% (last 7 days)
**Previous period**: 62% (prior 7 days)
**Trend**: ↑ 3% improvement

**Unresolved conversations analyzed**: 75

### Top Unresolved Patterns

| Pattern | Volume | Failure Reason | Potential AR Lift |
|---------|--------|----------------|-------------------|
| Order cancellation requests | 23 | Action limitation | +5% |
| Complex return scenarios | 18 | Knowledge gap | +4% |
| Account access issues | 12 | Handoff trigger | +2% |

### Recommendations

#### 1. Order Cancellation (Highest Impact)
**Problem**: Agent can't cancel orders; always hands off
**Solution**: 
- Create action integration with order management system
- Add playbook for cancellation flow
**Expected impact**: +5% AR

#### 2. Complex Returns
**Problem**: Return policy article doesn't cover exchanges or partial returns
**Solution**:
- Expand "Returns" knowledge article
- Add coaching for edge cases
**Expected impact**: +4% AR

#### 3. Account Access
**Problem**: Agent hands off on all password reset requests
**Solution**:
- Review handoff trigger rules
- Add self-service password reset playbook
**Expected impact**: +2% AR
```

## Tips for better AR analysis

- Focus on high-volume patterns first (biggest AR lift potential)
- Distinguish between solvable gaps vs. intentional handoffs
- Consider whether some handoffs are appropriate (complex issues, VIP customers)
- Track AR by topic/intent if possible to identify specific weak areas
- Recommend quick wins alongside larger initiatives
