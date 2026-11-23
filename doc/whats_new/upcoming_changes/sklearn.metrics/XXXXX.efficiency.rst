- :func:`metrics.ndcg_score` and :func:`metrics.dcg_score` are now several times
  faster with the default ``ignore_ties=False``, as the tie-averaged DCG is
  computed for all samples at once instead of in a Python loop over samples. The
  speed-up is largest (up to ~25x) with many samples and few labels per sample, and
  smaller (around 1.5x) when each sample has thousands of labels.
  By :user:`Saswat <saswattulo>`.
