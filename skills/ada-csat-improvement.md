---
name: ada-csat-improvement
description: Analyze CSAT performance and get actionable improvement recommendations using Ada's AI agent data. Use when the user asks about improving customer satisfaction, CSAT scores, low ratings, or wants to understand why customers are dissatisfied with their Ada chatbot.
license: Apache-2.0
compatibility: Requires Ada MCP server connected to Claude Desktop or compatible MCP client
metadata:
  author: ada
  version: "1.0"
allowed-tools: get_ada_metric get_available_filters get_conversations_by_filters get_conversation get_ada_configuration search_knowledge search_coaching
---

# Improving CSAT with Ada

## When to use this skill

Use this skill when the user wants to:
- Improve their CSAT score
- Understand why customers are giving low satisfaction ratings
- Get actionable recommendations for improving customer experience
- Analyze patterns in negative feedback
- Identify gaps in their AI agent's responses

## Workflow

### Step 1: Get current CSAT metrics

Start by understanding the baseline:

```
Use get_ada_metric to retrieve CSAT rate for the last 7 days (or user-specified timeframe)
```

Report the current CSAT percentage and compare to any available historical data.

### Step 2: Identify low-CSAT conversations

Use filtering to find problem areas:

```
1. Use get_available_filters to see available filter options
2. Use get_conversations_by_filters with CSAT scores of 1-2 to find low-satisfaction conversations
3. Request 50-100 conversations for meaningful pattern analysis
```

### Step 3: Analyze conversation patterns

Pull transcripts and summaries to understand root causes:

```
Use get_conversation on a sample of 10-20 low-CSAT conversations
```

Look for:
- Common customer inquiries that led to dissatisfaction
- Points where the agent's response was unhelpful
- Missing information or incorrect answers
- Tone or empathy issues
- Handoff failures or delays

### Step 4: Review current configuration

Understand what the agent is working with:

```
Use get_ada_configuration to retrieve:
- Playbooks
- Guidance/custom instructions
- Actions
- Coaching rules
- Company description
```

### Step 5: Search for gaps

Check if relevant content exists:

```
1. Use search_knowledge with topics from low-CSAT conversations
2. Use search_coaching to find relevant coaching rules
```

Identify:
- Topics with no knowledge coverage
- Outdated or incomplete articles
- Missing coaching for common scenarios

### Step 6: Provide actionable recommendations

Structure recommendations as:

1. **Quick wins** - Changes that can improve CSAT immediately
   - New coaching rules for common failure patterns
   - Updates to existing knowledge articles
   - Tone/empathy guidance additions

2. **Medium-term improvements** - Changes requiring more effort
   - New playbooks for uncovered scenarios
   - Knowledge base expansions
   - Action integrations

3. **Strategic changes** - Longer-term considerations
   - Process changes
   - Integration improvements
   - Training data updates

## Example output format

```markdown
## CSAT Analysis Summary

**Current CSAT**: 72% (last 7 days)
**Conversations analyzed**: 50 low-CSAT conversations

### Key Findings

1. **Refund policy confusion** (15 conversations)
   - Customers frustrated by unclear refund timeline
   - Agent responses lack specific day counts

2. **Shipping status inquiries** (12 conversations)
   - Agent can't access real-time tracking
   - Customers handed off unnecessarily

### Recommendations

#### Quick Wins
- Add coaching: "When discussing refunds, always mention the 5-7 business day processing time"
- Update knowledge article "Refund Policy" with specific timelines

#### Medium-Term
- Create playbook for shipping status that integrates with tracking API
- Add action to pull order status from backend system
```

## Tips for better analysis

- Be specific about timeframes when querying metrics
- Analyze at least 50 conversations for meaningful patterns
- Cross-reference findings with current configuration
- Prioritize recommendations by potential CSAT impact
- Consider both content gaps AND tone/empathy issues
