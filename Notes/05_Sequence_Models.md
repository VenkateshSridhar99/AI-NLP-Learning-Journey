# 🔁 Sequence Models (Days 7–8)

## Why They’re Different:
Standard ML assumes inputs are independent.  
But language, speech, and time-series need memory. That’s where **RNNs** come in.

### Key Models:
- **RNN**: Has memory, but forgets long-term dependencies.
- **LSTM**: Fixed that with gates and a memory cell.
- **GRU**: Simpler than LSTM but similar performance.

### Problem I Learned:
- **Vanishing Gradient**: Makes RNNs bad at remembering long-range patterns.
- Solution? LSTM/GRU.

## Application:
Now I see how chatbots, speech-to-text, and predictive text actually work. It's not magic — it's memory and math.