# Money Distribution Hypothesis

A Monte Carlo simulation demonstrating how wealth distributes in a population under different economic scenarios.

## Overview

This project simulates a world where people randomly give money to each other each day, and observes how wealth inequality emerges under various conditions. Each simulation runs for 10,000 days and visualizes the distribution at key checkpoints (day 0, 100, 1000, and 10000).

## Simulation Scenarios

### World #0: Perfect Equality with Safety Net
- **Conditions**: Equal starting wealth, no debt allowed
- **Key Finding**: Even with equal conditions, random transactions create inequality, but a safety net prevents extreme poverty

### World #1: Perfect Equality with Debt
- **Conditions**: Equal starting wealth, debt is allowed
- **Key Finding**: Random transactions naturally lead to wealth concentration, with some people accumulating significant debt

### World #2: Wealth Inequality (Rich Second Generation)
- **Conditions**: 90 normal people (100 cash) + 10 rich people (200 cash)
- **Key Finding**: Initial wealth advantages tend to persist but don't guarantee staying wealthy

### World #3: Full Wealth Spectrum
- **Conditions**: 80 normal (100) + 10 rich (200) + 10 poor (50)
- **Key Finding**: Starting position matters, but randomness can overcome initial disadvantages

### World #4: Charm/Network Effects
- **Conditions**: Equal wealth, but 10 people have 1% higher probability of receiving money
- **Key Finding**: Small advantages in social connections compound significantly over time

### World #5: Progressive Taxation
- **Conditions**: Wealth inequality + 20% tax on wealth above 150 (redistributed every 100 days)
- **Key Finding**: Progressive taxation reduces wealth inequality while maintaining incentives

### World #6: Universal Basic Income (UBI)
- **Conditions**: Wealth inequality + everyone receives 0.5 units daily
- **Key Finding**: UBI provides a floor for wealth but doesn't prevent inequality at the top

### World #7: Speculative/Gambling Behavior
- **Conditions**: 90 normal people + 10 gamblers who bet random amounts (1-5 units)
- **Key Finding**: High-risk behavior leads to extreme outcomes - both very rich and very poor

### World #8: Transaction Costs
- **Conditions**: 10% fee on every transaction (wealth disappears)
- **Key Finding**: Intermediary costs gradually drain total wealth from the system

### World #9: Wealth Cap
- **Conditions**: Maximum personal wealth of 200, excess redistributed every 50 days
- **Key Finding**: Wealth caps create more equal distribution but may reduce accumulation incentives

### World #10: Combined Realistic Economy
- **Conditions**: Wealth inequality + charm effect + UBI + progressive taxation
- **Key Finding**: Multiple policies working together can balance growth with equality

### World #11: Productivity & Economic Growth
- **Conditions**: 20% of people are "producers" who create 0.5-1.5 units daily
- **Key Finding**: Productivity creates real economic growth, not just wealth redistribution

## Key Insights

1. **Randomness Creates Inequality**: Even starting from perfect equality, random transactions naturally lead to wealth concentration
2. **Compound Effects**: Small advantages (like charm/network effects) compound significantly over time
3. **Policy Matters**: Different economic policies (taxation, UBI, wealth caps) have measurable effects on distribution
4. **Growth vs Redistribution**: Productivity-based systems create wealth, while most other scenarios just redistribute existing wealth
5. **Transaction Costs Matter**: Fees and intermediaries gradually drain wealth from the economy

## How to Run

```python
# Run all scenarios
world_0()  # Equality + Safety Net
world_1()  # Equality + Debt
world_2()  # Rich Second Generation
world_3()  # Full Wealth Spectrum
world_4()  # Charm/Network Effects
world_5()  # Progressive Taxation
world_6()  # Universal Basic Income
world_7()  # Gambling Behavior
world_8()  # Transaction Costs
world_9()  # Wealth Cap
world_10() # Combined Realistic Economy
world_11() # Productivity & Growth
```

## Technical Details

- **Simulation**: Monte Carlo method with 100 agents over 10,000 iterations
- **Visualization**: Bar charts showing wealth distribution (both original order and sorted)
- **Color Coding**:
  - Red = Rich people
  - Lime/Green = Poor people
  - Orange = Charming people
  - Purple = Gamblers
  - Gold = Producers

## Dependencies

- numpy
- matplotlib

## What This Demonstrates

This simulation helps visualize:
- How wealth inequality emerges naturally from random transactions
- The effects of different economic policies on wealth distribution
- Why initial conditions and small advantages matter
- The difference between zero-sum redistribution and productive growth
- How transaction costs affect overall economic health
