- :func:`metrics.ndcg_score` and :func:`metrics.dcg_score` are now several times
  faster (up to ~25x when there are many samples) with the default
  ``ignore_ties=False``, as the tie-averaged DCG is computed for all samples at
  once instead of in a Python loop over samples.
  By :user:`Saswat <saswattulo>`.
