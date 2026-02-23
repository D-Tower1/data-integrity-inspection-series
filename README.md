# The Cost of a Single Bad Tick


In any distributed financial system, corruption rarely announces itself. It appears quietly—one incorrect
price print, a duplicated bar, a timestamp shifted by a minute, or a partial file write that still parses
correctly. The danger is not the existence of a single defect. The danger is propagation. One bad tick
feeds aggregation, influences volatility readings, shifts indicator calculations, and silently alters
research conclusions. By the time it is detected—if it is detected—it is no longer local. It is structural.
Time series systems depend on continuity, monotonic timestamp progression, and arithmetic integrity
inside each OHLC bar. A single anomalous extreme can distort ATR calculations for multiple future
windows. A timestamp shift can misalign rolling averages. Duplicate rows can inflate volume. None of
these errors trigger dramatic system failures. They simply introduce bias. Without deterministic
validation—expected bar counts, fixed interval deltas, UTC normalization, logical OHLC
constraints—silent corruption becomes accepted input.
Inspection-first systems assume failure is possible at all times. They enforce strict interval validation,
reject datasets that deviate from expected structure, and archive canonical raw data immutably before
transformation. Clean data does not ensure profitability. It ensures that performance metrics reflect
market behavior rather than upstream distortion. The cost of a single bad tick is not measured in cents.
It is measured in structural credibility and long-term trust.
