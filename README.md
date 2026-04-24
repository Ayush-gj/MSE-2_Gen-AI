# KIET_AI_DebugChallenge

# Bugs
Bug 1 (Threshold): Reduced CONFIDENCE_THRESHOLD from 0.95 to 0.60 to allow the bot to respond when it has a reasonable but not absolute certainty.

Bug 2 (Filtering): Changed tok.isdigit() to tok.isalpha() in preprocess so the bot processes words instead of ignoring everything except numbers.

Bug 3 (Encoding): Fixed _one_hot by setting vec[idx] = 1.0 instead of 0.0, ensuring tokens have a non-zero mathematical representation.

Bug 4 (Gradients): Corrected the $tanh$ derivative in the backward pass from (1.0 + self._hs[t + 1] ** 2) to (1.0 - self._hs[t + 1] ** 2).

Bug 5 (Convergence): Decreased the convergence loss limit from 0.05 to 0.01 to ensure the model trains long enough to reach high accuracy.
