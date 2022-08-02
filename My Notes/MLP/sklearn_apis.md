

## [*DictVectorizer*](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.DictVectorizer.html?highlight=dictvectorizer)
  class sklearn.feature_extraction.DictVectorizer(*, dtype=<class 'numpy.float64'>, separator='=', sparse=True, sort=True)[source]¶

  #### *List of parameters:*
  - **X** : Mapping or iterable over Mappings
  - **y** : (ignored)
  - **X** : Mapping or iterable over Mappings
  - **y** : (ignored)

  #### *List of return values:*

  #### *List of attributes:*
  - **self** : object
  - **Xa** : {array, sparse matrix}

  #### *List of methods:*
  - **fit(X[, y])** : Learn a list of feature name -> indices mappings.
  - **fit_transform(X[, y])** : Learn a list of feature name -> indices mappings and transform X.
  - **get_feature_names()** : DEPRECATED: get_feature_names is deprecated in 1.0 and will be removed in 1.2.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(X[, dict_type])** : Transform array or sparse matrix X back to feature mappings.
  - **restrict(support[, indices])** : Restrict the features to those in support using feature selection.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Transform feature->value dicts to array or sparse matrix.


## [*TfidfVectorizer*](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html?highlight=tfidfvectorizer)
  class sklearn.feature_extraction.text.TfidfVectorizer(*, input='content', encoding='utf-8', decode_error='strict', strip_accents=None, lowercase=True, preprocessor=None, tokenizer=None, analyzer='word', stop_words=None, token_pattern='(?u)\\b\\w\\w+\\b', ngram_range=(1, 1), max_df=1.0, min_df=1, max_features=None, vocabulary=None, binary=False, dtype=<class 'numpy.float64'>, norm='l2', use_idf=True, smooth_idf=True, sublinear_tf=False)[source]¶

  #### *List of parameters:*
  - **input** : {‘filename’, ‘file’, ‘content’}, default=’content’
  - **encoding** : str, default=’utf-8’
  - **decode_error** : {‘strict’, ‘ignore’, ‘replace’}, default=’strict’
  - **strip_accents** : {‘ascii’, ‘unicode’}, default=None
  - **lowercase** : bool, default=True
  - **preprocessor** : callable, default=None
  - **tokenizer** : callable, default=None
  - **analyzer** : {‘word’, ‘char’, ‘char_wb’} or callable, default=’word’
  - **stop_words** : {‘english’}, list, default=None
  - **token_pattern** : str, default=r”(?u)\b\w\w+\b”
  - **ngram_range** : tuple (min_n, max_n), default=(1, 1)
  - **max_df** : float or int, default=1.0
  - **min_df** : float or int, default=1
  - **max_features** : int, default=None
  - **vocabulary** : Mapping or iterable, default=None
  - **binary** : bool, default=False
  - **dtype** : dtype, default=float64
  - **norm** : {‘l1’, ‘l2’}, default=’l2’
  - **use_idf** : bool, default=True
  - **smooth_idf** : bool, default=True
  - **sublinear_tf** : bool, default=False

  #### *List of attributes:*

  #### *List of attributes:*
  - **vocabulary_** : dict
  - **fixed_vocabulary_** : bool
  - **stop_words_** : array of shape (n_features,)

  #### *List of methods:*
  - **build_analyzer()** : Return a callable to process input data.
  - **build_preprocessor()** : Return a function to preprocess the text before tokenization.
  - **build_tokenizer()** : Return a function that splits a string into a sequence of tokens.
  - **decode(doc)** : Decode the input into a string of unicode symbols.
  - **fit(raw_documents[, y])** : Learn vocabulary and idf from training set.
  - **fit_transform(raw_documents[, y])** : Learn vocabulary and idf, return document-term matrix.
  - **get_feature_names()** : DEPRECATED: get_feature_names is deprecated in 1.0 and will be removed in 1.2.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **get_stop_words()** : Build or fetch the effective stop words list.
  - **inverse_transform(X)** : Return terms per document with nonzero entries in X.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(raw_documents)** : Transform documents to document-term matrix.


## [*CountVectorizer*](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.CountVectorizer.html)
  class sklearn.feature_extraction.text.CountVectorizer(*, input='content', encoding='utf-8', decode_error='strict', strip_accents=None, lowercase=True, preprocessor=None, tokenizer=None, stop_words=None, token_pattern='(?u)\\b\\w\\w+\\b', ngram_range=(1, 1), analyzer='word', max_df=1.0, min_df=1, max_features=None, vocabulary=None, binary=False, dtype=<class 'numpy.int64'>)[source]¶

  #### *List of parameters:*
  - **input** : {‘filename’, ‘file’, ‘content’}, default=’content’
  - **encoding** : str, default=’utf-8’
  - **decode_error** : {‘strict’, ‘ignore’, ‘replace’}, default=’strict’
  - **strip_accents** : {‘ascii’, ‘unicode’}, default=None
  - **lowercase** : bool, default=True
  - **preprocessor** : callable, default=None
  - **tokenizer** : callable, default=None
  - **stop_words** : {‘english’}, list, default=None
  - **token_pattern** : str, default=r”(?u)\b\w\w+\b”
  - **ngram_range** : tuple (min_n, max_n), default=(1, 1)
  - **analyzer** : {‘word’, ‘char’, ‘char_wb’} or callable, default=’word’
  - **max_df** : float in range [0.0, 1.0] or int, default=1.0
  - **min_df** : float in range [0.0, 1.0] or int, default=1
  - **max_features** : int, default=None
  - **vocabulary** : Mapping or iterable, default=None
  - **binary** : bool, default=False
  - **dtype** : type, default=np.int64

  #### *List of attributes:*

  #### *List of attributes:*
  - **vocabulary_** : dict
  - **fixed_vocabulary_** : bool
  - **stop_words_** : set

  #### *List of methods:*
  - **build_analyzer()** : Return a callable to process input data.
  - **build_preprocessor()** : Return a function to preprocess the text before tokenization.
  - **build_tokenizer()** : Return a function that splits a string into a sequence of tokens.
  - **decode(doc)** : Decode the input into a string of unicode symbols.
  - **fit(raw_documents[, y])** : Learn a vocabulary dictionary of all tokens in the raw documents.
  - **fit_transform(raw_documents[, y])** : Learn the vocabulary dictionary and return document-term matrix.
  - **get_feature_names()** : DEPRECATED: get_feature_names is deprecated in 1.0 and will be removed in 1.2.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **get_stop_words()** : Build or fetch the effective stop words list.
  - **inverse_transform(X)** : Return terms per document with nonzero entries in X.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(raw_documents)** : Transform documents to document-term matrix.


## [*VarianceThreshold*](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.VarianceThreshold.html?highlight=variancethreshold)
  class sklearn.feature_selection.VarianceThreshold(threshold=0.0)[source]¶

  #### *List of parameters:*
  - **threshold** : float, default=0

  #### *List of attributes:*

  #### *List of attributes:*
  - **variances_** : array, shape (n_features,)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X[, y])** : Learn empirical variances from X.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Mask feature names according to selected features.
  - **get_params([deep])** : Get parameters for this estimator.
  - **get_support([indices])** : Get a mask, or integer index, of the features selected.
  - **inverse_transform(X)** : Reverse the transformation operation.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Reduce X to the selected features.


## [*SelectKBest*](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html?highlight=selectkbest)
  class sklearn.feature_selection.SelectKBest(score_func=<function f_classif>, *, k=10)[source]¶

  #### *List of parameters:*
  - **score_func** : callable, default=f_classif
  - **k** : int or “all”, default=10

  #### *List of attributes:*

  #### *List of attributes:*
  - **scores_** : array-like of shape (n_features,)
  - **pvalues_** : array-like of shape (n_features,)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X, y)** : Run score function on (X, y) and get the appropriate features.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Mask feature names according to selected features.
  - **get_params([deep])** : Get parameters for this estimator.
  - **get_support([indices])** : Get a mask, or integer index, of the features selected.
  - **inverse_transform(X)** : Reverse the transformation operation.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Reduce X to the selected features.


## [*SelectPercentile*](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectPercentile.html?highlight=selectpercentile)
  class sklearn.feature_selection.SelectPercentile(score_func=<function f_classif>, *, percentile=10)[source]¶

  #### *List of parameters:*
  - **score_func** : callable, default=f_classif
  - **percentile** : int, default=10

  #### *List of attributes:*

  #### *List of attributes:*
  - **scores_** : array-like of shape (n_features,)
  - **pvalues_** : array-like of shape (n_features,)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X, y)** : Run score function on (X, y) and get the appropriate features.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Mask feature names according to selected features.
  - **get_params([deep])** : Get parameters for this estimator.
  - **get_support([indices])** : Get a mask, or integer index, of the features selected.
  - **inverse_transform(X)** : Reverse the transformation operation.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Reduce X to the selected features.


## [*GenericUnivariateSelect*](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.GenericUnivariateSelect.html?highlight=genericunivariateselect)
  class sklearn.feature_selection.GenericUnivariateSelect(score_func=<function f_classif>, *, mode='percentile', param=1e-05)[source]¶

  #### *List of parameters:*
  - **score_func** : callable, default=f_classif
  - **mode** : {‘percentile’, ‘k_best’, ‘fpr’, ‘fdr’, ‘fwe’}, default=’percentile’
  - **param** : float or int depending on the feature selection mode, default=1e-5

  #### *List of attributes:*

  #### *List of attributes:*
  - **scores_** : array-like of shape (n_features,)
  - **pvalues_** : array-like of shape (n_features,)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X, y)** : Run score function on (X, y) and get the appropriate features.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Mask feature names according to selected features.
  - **get_params([deep])** : Get parameters for this estimator.
  - **get_support([indices])** : Get a mask, or integer index, of the features selected.
  - **inverse_transform(X)** : Reverse the transformation operation.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Reduce X to the selected features.


## [*RFE*](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.RFE.html)
  class sklearn.feature_selection.RFE(estimator, *, n_features_to_select=None, step=1, verbose=0, importance_getter='auto')[source]¶

  #### *List of parameters:*
  - **estimator** : Estimator instance
  - **n_features_to_select** : int or float, default=None
  - **step** : int or float, default=1
  - **verbose** : int, default=0
  - **importance_getter** : str or callable, default=’auto’
  - **X** : array of shape [n_samples, n_features]
  - **y** : array of shape [n_samples]
  - ****fit_params** : dict

  #### *List of attributes:*

  #### *List of attributes:*
  - **estimator_** : ndarray of shape (n_classes,)
  - **n_features_** : Estimator instance
  - **n_features_in_** : int
  - **feature_names_in_** : int
  - **ranking_** : ndarray of shape (n_features_in_,)
  - **support_** : ndarray of shape (n_features,)
  - **score** : ndarray of shape (n_features,)

  #### *List of methods:*
  - **decision_function(X)** : Compute the decision function of X.
  - **fit(X, y, \*\*fit_params)** : Fit the RFE model and then the underlying estimator on the selected features.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Mask feature names according to selected features.
  - **get_params([deep])** : Get parameters for this estimator.
  - **get_support([indices])** : Get a mask, or integer index, of the features selected.
  - **inverse_transform(X)** : Reverse the transformation operation.
  - **predict(X)** : Reduce X to the selected features and then predict using the underlying estimator.
  - **predict_log_proba(X)** : Predict class log-probabilities for X.
  - **predict_proba(X)** : Predict class probabilities for X.
  - **score(X, y, \*\*fit_params)** : Reduce X to the selected features and return the score of the underlying estimator.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Reduce X to the selected features.


## [*RFECV*](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.RFECV.html)
  class sklearn.feature_selection.RFECV(estimator, *, step=1, min_features_to_select=1, cv=None, scoring=None, verbose=0, n_jobs=None, importance_getter='auto')[source]¶

  #### *List of parameters:*
  - **estimator** : Estimator instance
  - **step** : int or float, default=1
  - **min_features_to_select** : int, default=1
  - **cv** : int, cross-validation generator or an iterable, default=None
  - **scoring** : str, callable or None, default=None
  - **verbose** : int, default=0
  - **n_jobs** : int or None, default=None
  - **importance_getter** : str or callable, default=’auto’
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,)
  - **groups** : array-like of shape (n_samples,) or None, default=None
  - **X** : array of shape [n_samples, n_features]
  - **y** : array of shape [n_samples]
  - ****fit_params** : dict

  #### *List of attributes:*

  #### *List of attributes:*
  - **estimator_** : ndarray of shape (n_classes,)
  - **cv_results_** : Estimator instance
  - **n_features_** : ndarray of shape (n_subsets_of_features,)
  - **n_features_in_** : dict of ndarrays
  - **feature_names_in_** : int
  - **ranking_** : int
  - **support_** : ndarray of shape (n_features_in_,)
  - **self** : narray of shape (n_features,)
  - **score** : ndarray of shape (n_features,)

  #### *List of methods:*
  - **decision_function(X)** : Compute the decision function of X.
  - **fit(X, y[, groups])** : Fit the RFE model and automatically tune the number of selected features.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Mask feature names according to selected features.
  - **get_params([deep])** : Get parameters for this estimator.
  - **get_support([indices])** : Get a mask, or integer index, of the features selected.
  - **inverse_transform(X)** : Reverse the transformation operation.
  - **predict(X)** : Reduce X to the selected features and then predict using the underlying estimator.
  - **predict_log_proba(X)** : Predict class log-probabilities for X.
  - **predict_proba(X)** : Predict class probabilities for X.
  - **score(X, y, \*\*fit_params)** : Reduce X to the selected features and return the score of the underlying estimator.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Reduce X to the selected features.


## [*SelectFromModel*](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectFromModel.html)
  class sklearn.feature_selection.SelectFromModel(estimator, *, threshold=None, prefit=False, norm_order=1, max_features=None, importance_getter='auto')[source]¶

  #### *List of parameters:*
  - **estimator** : object
  - **threshold** : str or float, default=None
  - **prefit** : bool, default=False
  - **norm_order** : non-zero int, inf, -inf, default=1
  - **max_features** : int, callable, default=None
  - **importance_getter** : str or callable, default=’auto’

  #### *List of attributes:*

  #### *List of attributes:*
  - **estimator_** : estimator
  - **max_features_** : int
  - **feature_names_in_** : int

  #### *List of methods:*
  - **fit(X[, y])** : Fit the SelectFromModel meta-transformer.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Mask feature names according to selected features.
  - **get_params([deep])** : Get parameters for this estimator.
  - **get_support([indices])** : Get a mask, or integer index, of the features selected.
  - **inverse_transform(X)** : Reverse the transformation operation.
  - **partial_fit(X[, y])** : Fit the SelectFromModel meta-transformer only once.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Reduce X to the selected features.


## [*SequentialFeatureSelector*](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SequentialFeatureSelector.html)
  class sklearn.feature_selection.SequentialFeatureSelector(estimator, *, n_features_to_select='warn', tol=None, direction='forward', scoring=None, cv=5, n_jobs=None)[source]¶

  #### *List of parameters:*
  - **estimator** : estimator instance
  - **n_features_to_select** : “auto”, int or float, default=’warn’
  - **tol** : float, default=None
  - **direction** : {‘forward’, ‘backward’}, default=’forward’
  - **scoring** : str, callable, list/tuple or dict, default=None
  - **cv** : int, cross-validation generator or an iterable, default=None
  - **n_jobs** : int, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)
  - **n_features_to_select_** : int
  - **support_** : ndarray of shape (n_features,), dtype=bool

  #### *List of methods:*
  - **fit(X[, y])** : Learn the features to select from X.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Mask feature names according to selected features.
  - **get_params([deep])** : Get parameters for this estimator.
  - **get_support([indices])** : Get a mask, or integer index, of the features selected.
  - **inverse_transform(X)** : Reverse the transformation operation.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Reduce X to the selected features.


## [*SimpleImputer*](https://scikit-learn.org/stable/modules/generated/sklearn.impute.SimpleImputer.html)
  class sklearn.impute.SimpleImputer(*, missing_values=nan, strategy='mean', fill_value=None, verbose='deprecated', copy=True, add_indicator=False)[source]¶

  #### *List of parameters:*
  - **missing_values** : int, float, str, np.nan, None or pandas.NA, default=np.nan
  - **strategy** : str, default=’mean’
  - **fill_value** : str or numerical value, default=None
  - **verbose** : int, default=0
  - **copy** : bool, default=True
  - **add_indicator** : bool, default=False

  #### *List of attributes:*

  #### *List of attributes:*
  - **statistics_** : array of shape (n_features,)
  - **indicator_** : MissingIndicator
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X[, y])** : Fit the imputer on X.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(X)** : Convert the data back to the original representation.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Impute all missing values in X.


## [*KNNImputer*](https://scikit-learn.org/stable/modules/generated/sklearn.impute.KNNImputer.html)
  class sklearn.impute.KNNImputer(*, missing_values=nan, n_neighbors=5, weights='uniform', metric='nan_euclidean', copy=True, add_indicator=False)[source]¶

  #### *List of parameters:*
  - **missing_values** : int, float, str, np.nan or None, default=np.nan
  - **n_neighbors** : int, default=5
  - **weights** : {‘uniform’, ‘distance’} or callable, default=’uniform’
  - **metric** : {‘nan_euclidean’} or callable, default=’nan_euclidean’
  - **copy** : bool, default=True
  - **add_indicator** : bool, default=False

  #### *List of attributes:*

  #### *List of attributes:*
  - **indicator_** : MissingIndicator
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X[, y])** : Fit the imputer on X.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Impute all missing values in X.


## [*MissingIndicator*](https://scikit-learn.org/stable/modules/generated/sklearn.impute.MissingIndicator.html)
  class sklearn.impute.MissingIndicator(*, missing_values=nan, features='missing-only', sparse='auto', error_on_new=True)[source]¶

  #### *List of parameters:*
  - **missing_values** : int, float, str, np.nan or None, default=np.nan
  - **features** : {‘missing-only’, ‘all’}, default=’missing-only’
  - **sparse** : bool or ‘auto’, default=’auto’
  - **error_on_new** : bool, default=True

  #### *List of attributes:*

  #### *List of attributes:*
  - **features_** : ndarray of shape (n_missing_features,) or (n_features,)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X[, y])** : Fit the transformer on X.
  - **fit_transform(X[, y])** : Generate missing values indicator for X.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Generate missing values indicator for X.


## [*StandardScaler*](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html)
  class sklearn.preprocessing.StandardScaler(*, copy=True, with_mean=True, with_std=True)[source]¶

  #### *List of parameters:*
  - **copy** : bool, default=True
  - **with_mean** : bool, default=True
  - **with_std** : bool, default=True
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : None
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : None
  - **sample_weight** : array-like of shape (n_samples,), default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **scale_** : ndarray of shape (n_features,) or None
  - **mean_** : ndarray of shape (n_features,) or None
  - **var_** : ndarray of shape (n_features,) or None
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)
  - **n_samples_seen_** : int or ndarray of shape (n_features,)
  - **self** : object
  - **self** : object

  #### *List of methods:*
  - **fit(X[, y, sample_weight])** : Compute the mean and std to be used for later scaling.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(X[, copy])** : Scale back the data to the original representation.
  - **partial_fit(X[, y, sample_weight])** : Online computation of mean and std on X for later scaling.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X[, copy])** : Perform standardization by centering and scaling.


## [*MinMaxScaler*](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html)
  class sklearn.preprocessing.MinMaxScaler(feature_range=(0, 1), *, copy=True, clip=False)[source]¶

  #### *List of parameters:*
  - **feature_range** : tuple (min, max), default=(0, 1)
  - **copy** : bool, default=True
  - **clip** : bool, default=False

  #### *List of attributes:*

  #### *List of attributes:*
  - **min_** : ndarray of shape (n_features,)
  - **scale_** : ndarray of shape (n_features,)
  - **data_min_** : ndarray of shape (n_features,)
  - **data_max_** : ndarray of shape (n_features,)
  - **data_range_** : ndarray of shape (n_features,)
  - **n_features_in_** : int
  - **n_samples_seen_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X[, y])** : Compute the minimum and maximum to be used for later scaling.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(X)** : Undo the scaling of X according to feature_range.
  - **partial_fit(X[, y])** : Online computation of min and max on X for later scaling.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Scale features of X according to feature_range.


## [*MaxAbsScaler*](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MaxAbsScaler.html)
  class sklearn.preprocessing.MaxAbsScaler(*, copy=True)[source]¶

  #### *List of parameters:*
  - **copy** : bool, default=True

  #### *List of attributes:*

  #### *List of attributes:*
  - **scale_** : ndarray of shape (n_features,)
  - **max_abs_** : ndarray of shape (n_features,)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)
  - **n_samples_seen_** : int

  #### *List of methods:*
  - **fit(X[, y])** : Compute the maximum absolute value to be used for later scaling.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(X)** : Scale back the data to the original representation.
  - **partial_fit(X[, y])** : Online computation of max absolute value of X for later scaling.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Scale the data.


## [*FunctionTransformer*](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.FunctionTransformer.html)
  class sklearn.preprocessing.FunctionTransformer(func=None, inverse_func=None, *, validate=False, accept_sparse=False, check_inverse=True, feature_names_out=None, kw_args=None, inv_kw_args=None)[source]¶

  #### *List of parameters:*
  - **func** : callable, default=None
  - **inverse_func** : callable, default=None
  - **validate** : bool, default=False
  - **accept_sparse** : bool, default=False
  - **check_inverse** : bool, default=True
  - **feature_names_out** : callable, ‘one-to-one’ or None, default=None
  - **kw_args** : dict, default=None
  - **inv_kw_args** : dict, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X[, y])** : Fit transformer by checking X.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(X)** : Transform X using the inverse function.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Transform X using the forward function.


## [*PolynomialFeatures*](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.PolynomialFeatures.html)
  class sklearn.preprocessing.PolynomialFeatures(degree=2, *, interaction_only=False, include_bias=True, order='C')[source]¶

  #### *List of parameters:*
  - **degree** : int or tuple (min_degree, max_degree), default=2
  - **interaction_only** : bool, default=False
  - **include_bias** : bool, default=True
  - **order** : {‘C’, ‘F’}, default=’C’
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)

  #### *List of attributes:*

  #### *List of attributes:*
  - **n_features_in_** : ndarray of shape (n_output_features_, n_features_in_)
  - **feature_names_in_** : int
  - **n_output_features_** : int
  - **XP** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X[, y])** : Compute number of output features.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names([input_features])** : DEPRECATED: get_feature_names is deprecated in 1.0 and will be removed in 1.2.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Transform data to polynomial features.


## [*KBinsDiscretizer*](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.KBinsDiscretizer.html)
  class sklearn.preprocessing.KBinsDiscretizer(n_bins=5, *, encode='onehot', strategy='quantile', dtype=None, subsample='warn', random_state=None)[source]¶

  #### *List of parameters:*
  - **n_bins** : int or array-like of shape (n_features,), default=5
  - **encode** : {‘onehot’, ‘onehot-dense’, ‘ordinal’}, default=’onehot’
  - **strategy** : {‘uniform’, ‘quantile’, ‘kmeans’}, default=’quantile’
  - **dtype** : {np.float32, np.float64}, default=None
  - **subsample** : int or None (default=’warn’)
  - **random_state** : int, RandomState instance or None, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **bin_edges_** : ndarray of ndarray of shape (n_features,)
  - **n_bins_** : ndarray of shape (n_features,), dtype=np.int_
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X[, y])** : Fit the estimator.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Get output feature names.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(Xt)** : Transform discretized data back to original feature space.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Discretize the data.


## [*OneHotEncoder*](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html)
  class sklearn.preprocessing.OneHotEncoder(*, categories='auto', drop=None, sparse=True, dtype=<class 'numpy.float64'>, handle_unknown='error', min_frequency=None, max_categories=None)[source]¶

  #### *List of parameters:*
  - **categories** : ‘auto’ or a list of array-like, default=’auto’
  - **drop** : {‘first’, ‘if_binary’} or an array-like of shape (n_features,),             default=None
  - **sparse** : bool, default=True
  - **dtype** : number type, default=float
  - **handle_unknown** : {‘error’, ‘ignore’, ‘infrequent_if_exist’},                      default=’error’
  - **min_frequency** : int or float, default=None
  - **max_categories** : int, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **categories_** : list of arrays
  - **drop_idx_** : array of shape (n_features,)
  - **n_features_in_** : list of ndarray
  - **feature_names_in_** : int

  #### *List of methods:*
  - **fit(X[, y])** : Fit OneHotEncoder to X.
  - **fit_transform(X[, y])** : Fit OneHotEncoder to X, then transform X.
  - **get_feature_names([input_features])** : DEPRECATED: get_feature_names is deprecated in 1.0 and will be removed in 1.2.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(X)** : Convert the data back to the original representation.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Transform X using one-hot encoding.


## [*OrdinalEncoder*](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OrdinalEncoder.html)
  class sklearn.preprocessing.OrdinalEncoder(*, categories='auto', dtype=<class 'numpy.float64'>, handle_unknown='error', unknown_value=None, encoded_missing_value=nan)[source]¶

  #### *List of parameters:*
  - **categories** : ‘auto’ or a list of array-like, default=’auto’
  - **dtype** : number type, default np.float64
  - **handle_unknown** : {‘error’, ‘use_encoded_value’}, default=’error’
  - **unknown_value** : int or np.nan, default=None
  - **encoded_missing_value** : int or np.nan, default=np.nan

  #### *List of attributes:*

  #### *List of attributes:*
  - **categories_** : list of arrays
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X[, y])** : Fit the OrdinalEncoder to X.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(X)** : Convert the data back to the original representation.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Transform X to ordinal codes.


## [*LabelBinarizer*](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.LabelBinarizer.html)
  class sklearn.preprocessing.LabelBinarizer(*, neg_label=0, pos_label=1, sparse_output=False)[source]¶

  #### *List of parameters:*
  - **Y** : {ndarray, sparse matrix} of shape (n_samples, n_classes)
  - **threshold** : float, default=None

  #### *List of return values:*

  #### *List of attributes:*
  - **y** : {ndarray, sparse matrix} of shape (n_samples,)

  #### *List of methods:*
  - **fit(y)** : Fit label binarizer.
  - **fit_transform(y)** : Fit label binarizer/transform multi-class labels to binary labels.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(Y[, threshold])** : Transform binary labels back to multi-class labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(y)** : Transform multi-class labels to binary labels.


## [*Normalizer*](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.Normalizer.html)
  class sklearn.preprocessing.Normalizer(norm='l2', *, copy=True)[source]¶

  #### *List of parameters:*
  - **norm** : {‘l1’, ‘l2’, ‘max’}, default=’l2’
  - **copy** : bool, default=True

  #### *List of attributes:*

  #### *List of attributes:*
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X[, y])** : Do nothing and return the estimator unchanged.
  - **fit_transform(X[, y])** : Fit to data, then transform it.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X[, copy])** : Scale each non zero row of X to unit norm.


## [*ColumnTransformer*](https://scikit-learn.org/stable/modules/generated/sklearn.compose.ColumnTransformer.html)
  class sklearn.compose.ColumnTransformer(transformers, *, remainder='drop', sparse_threshold=0.3, n_jobs=None, transformer_weights=None, verbose=False, verbose_feature_names_out=True)[source]¶

  #### *List of parameters:*
  - **transformers** : list of tuples
  - **remainder** : {‘drop’, ‘passthrough’} or estimator, default=’drop’
  - **sparse_threshold** : float, default=0.3
  - **n_jobs** : int, default=None
  - **transformer_weights** : dict, default=None
  - **verbose** : bool, default=False
  - **verbose_feature_names_out** : bool, default=True

  #### *List of attributes:*

  #### *List of attributes:*
  - **transformers_** : list
  - **sparse_output_** : Bunch
  - **output_indices_** : bool
  - **n_features_in_** : dict

  #### *List of methods:*
  - **fit(X[, y])** : Fit all transformers using X.
  - **fit_transform(X[, y])** : Fit all transformers, transform the data and concatenate results.
  - **get_feature_names()** : DEPRECATED: get_feature_names is deprecated in 1.0 and will be removed in 1.2.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **set_params(\*\*kwargs)** : Set the parameters of this estimator.
  - **transform(X)** : Transform X separately by each transformer, concatenate results.


## [*TransformedTargetRegressor*](https://scikit-learn.org/stable/modules/generated/sklearn.compose.TransformedTargetRegressor.html)
  class sklearn.compose.TransformedTargetRegressor(regressor=None, *, transformer=None, func=None, inverse_func=None, check_inverse=True)[source]¶

  #### *List of parameters:*
  - **regressor** : object, default=None
  - **transformer** : object, default=None
  - **func** : function, default=None
  - **inverse_func** : function, default=None
  - **check_inverse** : bool, default=True

  #### *List of attributes:*

  #### *List of attributes:*
  - **regressor_** : object
  - **transformer_** : object
  - **feature_names_in_** : int

  #### *List of methods:*
  - **fit(X, y, \*\*fit_params)** : Fit the model according to the given training data.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X, \*\*predict_params)** : Predict using the base regressor, applying inverse.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*LinearRegression*](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)
  class sklearn.linear_model.LinearRegression(*, fit_intercept=True, normalize='deprecated', copy_X=True, n_jobs=None, positive=False)[source]¶

  #### *List of parameters:*
  - **fit_intercept** : bool, default=True
  - **normalize** : bool, default=False
  - **copy_X** : bool, default=True
  - **n_jobs** : int, default=None
  - **positive** : bool, default=False
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,) or (n_samples, n_targets)
  - **sample_weight** : array-like of shape (n_samples,), default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **coef_** : array of shape (n_features, ) or (n_targets, n_features)
  - **rank_** : int
  - **singular_** : array of shape (min(X, y),)
  - **intercept_** : float or array of shape (n_targets,)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)
  - **self** : object

  #### *List of methods:*
  - **fit(X, y[, sample_weight])** : Fit linear model.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict using the linear model.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*SGDRegressor*](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.SGDRegressor.html)
  class sklearn.linear_model.SGDRegressor(loss='squared_error', *, penalty='l2', alpha=0.0001, l1_ratio=0.15, fit_intercept=True, max_iter=1000, tol=0.001, shuffle=True, verbose=0, epsilon=0.1, random_state=None, learning_rate='invscaling', eta0=0.01, power_t=0.25, early_stopping=False, validation_fraction=0.1, n_iter_no_change=5, warm_start=False, average=False)[source]¶

  #### *List of parameters:*
  - **loss** : str, default=’squared_error’
  - **penalty** : {‘l2’, ‘l1’, ‘elasticnet’}, default=’l2’
  - **alpha** : float, default=0.0001
  - **l1_ratio** : float, default=0.15
  - **fit_intercept** : bool, default=True
  - **max_iter** : int, default=1000
  - **tol** : float, default=1e-3
  - **shuffle** : bool, default=True
  - **verbose** : int, default=0
  - **epsilon** : float, default=0.1
  - **random_state** : int, RandomState instance, default=None
  - **learning_rate** : str, default=’invscaling’
  - **eta0** : float, default=0.01
  - **power_t** : float, default=0.25
  - **early_stopping** : bool, default=False
  - **validation_fraction** : float, default=0.1
  - **n_iter_no_change** : int, default=5
  - **warm_start** : bool, default=False
  - **average** : bool or int, default=False

  #### *List of attributes:*

  #### *List of attributes:*
  - **coef_** : ndarray of shape (n_features,)
  - **intercept_** : ndarray of shape (1,)
  - **n_iter_** : int
  - **t_** : int
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **densify()** : Convert coefficient matrix to dense array format.
  - **fit(X, y[, coef_init, intercept_init, ...])** : Fit linear model with Stochastic Gradient Descent.
  - **get_params([deep])** : Get parameters for this estimator.
  - **partial_fit(X, y[, sample_weight])** : Perform one epoch of stochastic gradient descent on given samples.
  - **predict(X)** : Predict using the linear model.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **sparsify()** : Convert coefficient matrix to sparse format.


## [*Lasso*](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Lasso.html)
  class sklearn.linear_model.Lasso(alpha=1.0, *, fit_intercept=True, normalize='deprecated', precompute=False, copy_X=True, max_iter=1000, tol=0.0001, warm_start=False, positive=False, random_state=None, selection='cyclic')[source]¶

  #### *List of parameters:*
  - **alpha** : float, default=1.0
  - **fit_intercept** : bool, default=True
  - **normalize** : bool, default=False
  - **precompute** : bool or array-like of shape (n_features, n_features),                 default=False
  - **copy_X** : bool, default=True
  - **max_iter** : int, default=1000
  - **tol** : float, default=1e-4
  - **warm_start** : bool, default=False
  - **positive** : bool, default=False
  - **random_state** : int, RandomState instance, default=None
  - **selection** : {‘cyclic’, ‘random’}, default=’cyclic’
  - **X** : {ndarray, sparse matrix} of (n_samples, n_features)
  - **y** : {ndarray, sparse matrix} of shape (n_samples,) or             (n_samples, n_targets)
  - **sample_weight** : float or array-like of shape (n_samples,), default=None
  - **check_input** : bool, default=True

  #### *List of attributes:*

  #### *List of attributes:*
  - **coef_** : ndarray of shape (n_features,) or (n_targets, n_features)
  - **dual_gap_** : float or ndarray of shape (n_targets,)
  - **intercept_** : sparse matrix of shape (n_features, 1) or             (n_targets, n_features)
  - **n_iter_** : float or ndarray of shape (n_targets,)
  - **n_features_in_** : int or list of int
  - **feature_names_in_** : int
  - **self** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X, y[, sample_weight, check_input])** : Fit model with coordinate descent.
  - **get_params([deep])** : Get parameters for this estimator.
  - **path(X, y, \*[, l1_ratio, eps, n_alphas, ...])** : Compute elastic net path with coordinate descent.
  - **predict(X)** : Predict using the linear model.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*LassoCV*](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LassoCV.html)
  class sklearn.linear_model.LassoCV(*, eps=0.001, n_alphas=100, alphas=None, fit_intercept=True, normalize='deprecated', precompute='auto', max_iter=1000, tol=0.0001, copy_X=True, cv=None, verbose=False, n_jobs=None, positive=False, random_state=None, selection='cyclic')[source]¶

  #### *List of parameters:*
  - **eps** : float, default=1e-3
  - **n_alphas** : int, default=100
  - **alphas** : ndarray, default=None
  - **fit_intercept** : bool, default=True
  - **normalize** : bool, default=False
  - **precompute** : ‘auto’, bool or array-like of shape             (n_features, n_features), default=’auto’
  - **max_iter** : int, default=1000
  - **tol** : float, default=1e-4
  - **copy_X** : bool, default=True
  - **cv** : int, cross-validation generator or iterable, default=None
  - **verbose** : bool or int, default=False
  - **n_jobs** : int, default=None
  - **positive** : bool, default=False
  - **random_state** : int, RandomState instance, default=None
  - **selection** : {‘cyclic’, ‘random’}, default=’cyclic’

  #### *List of attributes:*

  #### *List of attributes:*
  - **alpha_** : float
  - **coef_** : ndarray of shape (n_features,) or (n_targets, n_features)
  - **intercept_** : float or ndarray of shape (n_targets,)
  - **mse_path_** : ndarray of shape (n_alphas, n_folds)
  - **alphas_** : ndarray of shape (n_alphas,)
  - **dual_gap_** : float or ndarray of shape (n_targets,)
  - **n_iter_** : int
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X, y[, sample_weight])** : Fit linear model with coordinate descent.
  - **get_params([deep])** : Get parameters for this estimator.
  - **path(X, y, \*[, eps, n_alphas, alphas, ...])** : Compute Lasso path with coordinate descent.
  - **predict(X)** : Predict using the linear model.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*Ridge*](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Ridge.html)
  class sklearn.linear_model.Ridge(alpha=1.0, *, fit_intercept=True, normalize='deprecated', copy_X=True, max_iter=None, tol=0.001, solver='auto', positive=False, random_state=None)[source]¶

  #### *List of parameters:*
  - **alpha** : {float, ndarray of shape (n_targets,)}, default=1.0
  - **fit_intercept** : bool, default=True
  - **normalize** : bool, default=False
  - **copy_X** : bool, default=True
  - **max_iter** : int, default=None
  - **tol** : float, default=1e-3
  - **solver** : {‘auto’, ‘svd’, ‘cholesky’, ‘lsqr’, ‘sparse_cg’,             ‘sag’, ‘saga’, ‘lbfgs’}, default=’auto’
  - **positive** : bool, default=False
  - **random_state** : int, RandomState instance, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **coef_** : ndarray of shape (n_features,) or (n_targets, n_features)
  - **intercept_** : float or ndarray of shape (n_targets,)
  - **n_iter_** : None or ndarray of shape (n_targets,)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X, y[, sample_weight])** : Fit Ridge regression model.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict using the linear model.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*RidgeCV*](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.RidgeCV.html)
  class sklearn.linear_model.RidgeCV(alphas=(0.1, 1.0, 10.0), *, fit_intercept=True, normalize='deprecated', scoring=None, cv=None, gcv_mode=None, store_cv_values=False, alpha_per_target=False)[source]¶

  #### *List of parameters:*
  - **alphas** : ndarray of shape (n_alphas,), default=(0.1, 1.0, 10.0)
  - **fit_intercept** : bool, default=True
  - **normalize** : bool, default=False
  - **scoring** : str, callable, default=None
  - **cv** : int, cross-validation generator or an iterable, default=None
  - **gcv_mode** : {‘auto’, ‘svd’, ‘eigen’}, default=’auto’
  - **store_cv_values** : bool, default=False
  - **alpha_per_target** : bool, default=False

  #### *List of attributes:*

  #### *List of attributes:*
  - **cv_values_** : ndarray of shape (n_samples, n_alphas) or             shape (n_samples, n_targets, n_alphas), optional
  - **coef_** : ndarray of shape (n_features) or (n_targets, n_features)
  - **intercept_** : float or ndarray of shape (n_targets,)
  - **alpha_** : float or ndarray of shape (n_targets,)
  - **best_score_** : float or ndarray of shape (n_targets,)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X, y[, sample_weight])** : Fit Ridge regression model with cv.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict using the linear model.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*LogisticRegression*](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
  class sklearn.linear_model.LogisticRegression(penalty='l2', *, dual=False, tol=0.0001, C=1.0, fit_intercept=True, intercept_scaling=1, class_weight=None, random_state=None, solver='lbfgs', max_iter=100, multi_class='auto', verbose=0, warm_start=False, n_jobs=None, l1_ratio=None)[source]¶

  #### *List of parameters:*
  - **penalty** : {‘l1’, ‘l2’, ‘elasticnet’, ‘none’}, default=’l2’
  - **dual** : bool, default=False
  - **tol** : float, default=1e-4
  - **C** : float, default=1.0
  - **fit_intercept** : bool, default=True
  - **intercept_scaling** : float, default=1
  - **class_weight** : dict or ‘balanced’, default=None
  - **random_state** : int, RandomState instance, default=None
  - **solver** : {‘newton-cg’, ‘lbfgs’, ‘liblinear’, ‘sag’, ‘saga’},             default=’lbfgs’
  - **max_iter** : int, default=100
  - **multi_class** : {‘auto’, ‘ovr’, ‘multinomial’}, default=’auto’
  - **verbose** : int, default=0
  - **warm_start** : bool, default=False
  - **n_jobs** : int, default=None
  - **l1_ratio** : float, default=None
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,)
  - **sample_weight** : array-like of shape (n_samples,) default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **classes_** : ndarray of shape (n_classes, )
  - **coef_** : ndarray of shape (1, n_features) or (n_classes, n_features)
  - **intercept_** : ndarray of shape (1,) or (n_classes,)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)
  - **n_iter_** : ndarray of shape (n_classes,) or (1, )

  #### *List of methods:*
  - **decision_function(X)** : Predict confidence scores for samples.
  - **densify()** : Convert coefficient matrix to dense array format.
  - **fit(X, y[, sample_weight])** : Fit the model according to the given training data.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict class labels for samples in X.
  - **predict_log_proba(X)** : Predict logarithm of probability estimates.
  - **predict_proba(X)** : Probability estimates.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **sparsify()** : Convert coefficient matrix to sparse format.


## [*LogisticRegressionCV*](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegressionCV.html)
  class sklearn.linear_model.LogisticRegressionCV(*, Cs=10, fit_intercept=True, cv=None, dual=False, penalty='l2', scoring=None, solver='lbfgs', tol=0.0001, max_iter=100, class_weight=None, n_jobs=None, verbose=0, refit=True, intercept_scaling=1.0, multi_class='auto', random_state=None, l1_ratios=None)[source]¶

  #### *List of parameters:*
  - **Cs** : int or list of floats, default=10
  - **fit_intercept** : bool, default=True
  - **cv** : int or cross-validation generator, default=None
  - **dual** : bool, default=False
  - **penalty** : {‘l1’, ‘l2’, ‘elasticnet’}, default=’l2’
  - **scoring** : str or callable, default=None
  - **solver** : {‘newton-cg’, ‘lbfgs’, ‘liblinear’, ‘sag’, ‘saga’},             default=’lbfgs’
  - **tol** : float, default=1e-4
  - **max_iter** : int, default=100
  - **class_weight** : dict or ‘balanced’, default=None
  - **n_jobs** : int, default=None
  - **verbose** : int, default=0
  - **refit** : bool, default=True
  - **intercept_scaling** : float, default=1
  - **multi_class** : {‘auto, ‘ovr’, ‘multinomial’}, default=’auto’
  - **random_state** : int, RandomState instance, default=None
  - **l1_ratios** : list of float, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **classes_** : ndarray of shape (n_classes, )
  - **coef_** : ndarray of shape (1, n_features) or (n_classes, n_features)
  - **intercept_** : ndarray of shape (1,) or (n_classes,)
  - **Cs_** : ndarray of shape (n_cs)
  - **l1_ratios_** : ndarray of shape (n_l1_ratios)
  - **coefs_paths_** : ndarray of shape (n_folds, n_cs, n_features) or                    (n_folds, n_cs, n_features + 1)
  - **scores_** : dict
  - **C_** : ndarray of shape (n_classes,) or (n_classes - 1,)
  - **l1_ratio_** : ndarray of shape (n_classes,) or (n_classes - 1,)
  - **n_iter_** : ndarray of shape (n_classes, n_folds, n_cs) or (1, n_folds, n_cs)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **decision_function(X)** : Predict confidence scores for samples.
  - **densify()** : Convert coefficient matrix to dense array format.
  - **fit(X, y[, sample_weight])** : Fit the model according to the given training data.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict class labels for samples in X.
  - **predict_log_proba(X)** : Predict logarithm of probability estimates.
  - **predict_proba(X)** : Probability estimates.
  - **score(X, y[, sample_weight])** : Score using the scoring option on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **sparsify()** : Convert coefficient matrix to sparse format.


## [*SGDClassifier*](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.SGDClassifier.html)
  class sklearn.linear_model.SGDClassifier(loss='hinge', *, penalty='l2', alpha=0.0001, l1_ratio=0.15, fit_intercept=True, max_iter=1000, tol=0.001, shuffle=True, verbose=0, epsilon=0.1, n_jobs=None, random_state=None, learning_rate='optimal', eta0=0.0, power_t=0.5, early_stopping=False, validation_fraction=0.1, n_iter_no_change=5, class_weight=None, warm_start=False, average=False)[source]¶

  #### *List of parameters:*
  - **loss** : {‘hinge’, ‘log_loss’, ‘log’, ‘modified_huber’, ‘squared_hinge’,        ‘perceptron’, ‘squared_error’, ‘huber’, ‘epsilon_insensitive’,        ‘squared_epsilon_insensitive’}, default=’hinge’
  - **penalty** : {‘l2’, ‘l1’, ‘elasticnet’}, default=’l2’
  - **alpha** : float, default=0.0001
  - **l1_ratio** : float, default=0.15
  - **fit_intercept** : bool, default=True
  - **max_iter** : int, default=1000
  - **tol** : float, default=1e-3
  - **shuffle** : bool, default=True
  - **verbose** : int, default=0
  - **epsilon** : float, default=0.1
  - **n_jobs** : int, default=None
  - **random_state** : int, RandomState instance, default=None
  - **learning_rate** : str, default=’optimal’
  - **eta0** : float, default=0.0
  - **power_t** : float, default=0.5
  - **early_stopping** : bool, default=False
  - **validation_fraction** : float, default=0.1
  - **n_iter_no_change** : int, default=5
  - **class_weight** : dict, {class_label: weight} or “balanced”, default=None
  - **warm_start** : bool, default=False
  - **average** : bool or int, default=False

  #### *List of attributes:*

  #### *List of attributes:*
  - **coef_** : ndarray of shape (1, n_features) if n_classes == 2 else             (n_classes, n_features)
  - **intercept_** : ndarray of shape (1,) if n_classes == 2 else (n_classes,)
  - **n_iter_** : int
  - **loss_function_** : concrete LossFunction
  - **classes_** : array of shape (n_classes,)
  - **t_** : int
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **decision_function(X)** : Predict confidence scores for samples.
  - **densify()** : Convert coefficient matrix to dense array format.
  - **fit(X, y[, coef_init, intercept_init, ...])** : Fit linear model with Stochastic Gradient Descent.
  - **get_params([deep])** : Get parameters for this estimator.
  - **partial_fit(X, y[, classes, sample_weight])** : Perform one epoch of stochastic gradient descent on given samples.
  - **predict(X)** : Predict class labels for samples in X.
  - **predict_log_proba(X)** : Log of probability estimates.
  - **predict_proba(X)** : Probability estimates.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **sparsify()** : Convert coefficient matrix to sparse format.


## [*RidgeClassifier*](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.RidgeClassifier.html)
  class sklearn.linear_model.RidgeClassifier(alpha=1.0, *, fit_intercept=True, normalize='deprecated', copy_X=True, max_iter=None, tol=0.001, class_weight=None, solver='auto', positive=False, random_state=None)[source]¶

  #### *List of parameters:*
  - **alpha** : float, default=1.0
  - **fit_intercept** : bool, default=True
  - **normalize** : bool, default=False
  - **copy_X** : bool, default=True
  - **max_iter** : int, default=None
  - **tol** : float, default=1e-3
  - **class_weight** : dict or ‘balanced’, default=None
  - **solver** : {‘auto’, ‘svd’, ‘cholesky’, ‘lsqr’, ‘sparse_cg’,             ‘sag’, ‘saga’, ‘lbfgs’}, default=’auto’
  - **positive** : bool, default=False
  - **random_state** : int, RandomState instance, default=None
  - **X** : {ndarray, sparse matrix} of shape (n_samples, n_features)
  - **y** : ndarray of shape (n_samples,)
  - **sample_weight** : float or ndarray of shape (n_samples,), default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **coef_** : ndarray of shape (1, n_features) or (n_classes, n_features)
  - **intercept_** : float or ndarray of shape (n_targets,)
  - **n_iter_** : None or ndarray of shape (n_targets,)
  - **n_features_in_** : ndarray of shape (n_classes,)
  - **feature_names_in_** : int
  - **self** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **decision_function(X)** : Predict confidence scores for samples.
  - **fit(X, y[, sample_weight])** : Fit Ridge classifier model.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict class labels for samples in X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*RidgeClassifierCV*](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.RidgeClassifierCV.html)
  class sklearn.linear_model.RidgeClassifierCV(alphas=(0.1, 1.0, 10.0), *, fit_intercept=True, normalize='deprecated', scoring=None, cv=None, class_weight=None, store_cv_values=False)[source]¶

  #### *List of parameters:*
  - **alphas** : ndarray of shape (n_alphas,), default=(0.1, 1.0, 10.0)
  - **fit_intercept** : bool, default=True
  - **normalize** : bool, default=False
  - **scoring** : str, callable, default=None
  - **cv** : int, cross-validation generator or an iterable, default=None
  - **class_weight** : dict or ‘balanced’, default=None
  - **store_cv_values** : bool, default=False

  #### *List of attributes:*

  #### *List of attributes:*
  - **cv_values_** : ndarray of shape (n_samples, n_targets, n_alphas), optional
  - **coef_** : ndarray of shape (1, n_features) or (n_targets, n_features)
  - **intercept_** : float or ndarray of shape (n_targets,)
  - **alpha_** : float
  - **best_score_** : float
  - **n_features_in_** : ndarray of shape (n_classes,)
  - **feature_names_in_** : int

  #### *List of methods:*
  - **decision_function(X)** : Predict confidence scores for samples.
  - **fit(X, y[, sample_weight])** : Fit Ridge classifier with cv.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict class labels for samples in X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*Perceptron*](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Perceptron.html)
  class sklearn.linear_model.Perceptron(*, penalty=None, alpha=0.0001, l1_ratio=0.15, fit_intercept=True, max_iter=1000, tol=0.001, shuffle=True, verbose=0, eta0=1.0, n_jobs=None, random_state=0, early_stopping=False, validation_fraction=0.1, n_iter_no_change=5, class_weight=None, warm_start=False)[source]¶

  #### *List of parameters:*
  - **penalty** : {‘l2’,’l1’,’elasticnet’}, default=None
  - **alpha** : float, default=0.0001
  - **l1_ratio** : float, default=0.15
  - **fit_intercept** : bool, default=True
  - **max_iter** : int, default=1000
  - **tol** : float, default=1e-3
  - **shuffle** : bool, default=True
  - **verbose** : int, default=0
  - **eta0** : float, default=1
  - **n_jobs** : int, default=None
  - **random_state** : int, RandomState instance or None, default=0
  - **early_stopping** : bool, default=False
  - **validation_fraction** : float, default=0.1
  - **n_iter_no_change** : int, default=5
  - **class_weight** : dict, {class_label: weight} or “balanced”, default=None
  - **warm_start** : bool, default=False

  #### *List of attributes:*

  #### *List of attributes:*
  - **classes_** : ndarray of shape (n_classes,)
  - **coef_** : ndarray of shape (1, n_features) if n_classes == 2 else             (n_classes, n_features)
  - **intercept_** : ndarray of shape (1,) if n_classes == 2 else (n_classes,)
  - **loss_function_** : concrete LossFunction
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)
  - **n_iter_** : int
  - **t_** : int

  #### *List of methods:*
  - **decision_function(X)** : Predict confidence scores for samples.
  - **densify()** : Convert coefficient matrix to dense array format.
  - **fit(X, y[, coef_init, intercept_init, ...])** : Fit linear model with Stochastic Gradient Descent.
  - **get_params([deep])** : Get parameters for this estimator.
  - **partial_fit(X, y[, classes, sample_weight])** : Perform one epoch of stochastic gradient descent on given samples.
  - **predict(X)** : Predict class labels for samples in X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **sparsify()** : Convert coefficient matrix to sparse format.


## [*SVC*](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html)
  class sklearn.svm.SVC(*, C=1.0, kernel='rbf', degree=3, gamma='scale', coef0=0.0, shrinking=True, probability=False, tol=0.001, cache_size=200, class_weight=None, verbose=False, max_iter=- 1, decision_function_shape='ovr', break_ties=False, random_state=None)[source]¶

  #### *List of parameters:*
  - **C** : float, default=1.0
  - **kernel** : {‘linear’, ‘poly’, ‘rbf’, ‘sigmoid’, ‘precomputed’} or callable,          default=’rbf’
  - **degree** : int, default=3
  - **gamma** : {‘scale’, ‘auto’} or float, default=’scale’
  - **coef0** : float, default=0.0
  - **shrinking** : bool, default=True
  - **probability** : bool, default=False
  - **tol** : float, default=1e-3
  - **cache_size** : float, default=200
  - **class_weight** : dict or ‘balanced’, default=None
  - **verbose** : bool, default=False
  - **max_iter** : int, default=-1
  - **decision_function_shape** : {‘ovo’, ‘ovr’}, default=’ovr’
  - **break_ties** : bool, default=False
  - **random_state** : int, RandomState instance or None, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **class_weight_** : ndarray of shape (n_classes,)
  - **classes_** : ndarray of shape (n_classes,)
  - **dual_coef_** : ndarray of shape (n_classes * (n_classes - 1) / 2, n_features)
  - **fit_status_** : ndarray of shape (n_classes -1, n_SV)
  - **intercept_** : int
  - **n_features_in_** : ndarray of shape (n_classes * (n_classes - 1) / 2,)
  - **feature_names_in_** : int
  - **n_iter_** : ndarray of shape (n_features_in_,)
  - **support_** : ndarray of shape (n_classes * (n_classes - 1) // 2,)
  - **support_vectors_** : ndarray of shape (n_SV)
  - **shape_fit_** : ndarray of shape (n_SV, n_features)

  #### *List of methods:*
  - **decision_function(X)** : Evaluate the decision function for the samples in X.
  - **fit(X, y[, sample_weight])** : Fit the SVM model according to the given training data.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Perform classification on samples in X.
  - **predict_log_proba(X)** : Compute log probabilities of possible outcomes for samples in X.
  - **predict_proba(X)** : Compute probabilities of possible outcomes for samples in X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*LinearSVC*](https://scikit-learn.org/stable/modules/generated/sklearn.svm.LinearSVC.html)
  class sklearn.svm.LinearSVC(penalty='l2', loss='squared_hinge', *, dual=True, tol=0.0001, C=1.0, multi_class='ovr', fit_intercept=True, intercept_scaling=1, class_weight=None, verbose=0, random_state=None, max_iter=1000)[source]¶

  #### *List of parameters:*
  - **penalty** : {‘l1’, ‘l2’}, default=’l2’
  - **loss** : {‘hinge’, ‘squared_hinge’}, default=’squared_hinge’
  - **dual** : bool, default=True
  - **tol** : float, default=1e-4
  - **C** : float, default=1.0
  - **multi_class** : {‘ovr’, ‘crammer_singer’}, default=’ovr’
  - **fit_intercept** : bool, default=True
  - **intercept_scaling** : float, default=1
  - **class_weight** : dict or ‘balanced’, default=None
  - **verbose** : int, default=0
  - **random_state** : int, RandomState instance or None, default=None
  - **max_iter** : int, default=1000
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,)
  - **sample_weight** : array-like of shape (n_samples,), default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **coef_** : ndarray of shape (1, n_features) if n_classes == 2             else (n_classes, n_features)
  - **intercept_** : ndarray of shape (1,) if n_classes == 2 else (n_classes,)
  - **classes_** : ndarray of shape (n_classes,)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)
  - **n_iter_** : int
  - **self** : object

  #### *List of methods:*
  - **decision_function(X)** : Predict confidence scores for samples.
  - **densify()** : Convert coefficient matrix to dense array format.
  - **fit(X, y[, sample_weight])** : Fit the model according to the given training data.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict class labels for samples in X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **sparsify()** : Convert coefficient matrix to sparse format.


## [*MultinomialNB*](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html)
  class sklearn.naive_bayes.MultinomialNB(*, alpha=1.0, fit_prior=True, class_prior=None)[source]¶

  #### *List of parameters:*
  - **alpha** : float, default=1.0
  - **fit_prior** : bool, default=True
  - **class_prior** : array-like of shape (n_classes,), default=None
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,)
  - **classes** : array-like of shape (n_classes,), default=None
  - **sample_weight** : array-like of shape (n_samples,), default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **class_count_** : ndarray of shape (n_classes,)
  - **class_log_prior_** : ndarray of shape (n_classes,)
  - **classes_** : ndarray of shape (n_classes,)
  - **feature_count_** : ndarray of shape (n_classes, n_features)
  - **feature_log_prob_** : ndarray of shape (n_classes, n_features)
  - **n_features_in_** : int
  - **feature_names_in_** : int
  - **self** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X, y[, sample_weight])** : Fit Naive Bayes classifier according to X, y.
  - **get_params([deep])** : Get parameters for this estimator.
  - **partial_fit(X, y[, classes, sample_weight])** : Incremental fit on a batch of samples.
  - **predict(X)** : Perform classification on an array of test vectors X.
  - **predict_log_proba(X)** : Return log-probability estimates for the test vector X.
  - **predict_proba(X)** : Return probability estimates for the test vector X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*GaussianNB*](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.GaussianNB.html)
  class sklearn.naive_bayes.GaussianNB(*, priors=None, var_smoothing=1e-09)[source]¶

  #### *List of parameters:*
  - **priors** : array-like of shape (n_classes,)
  - **var_smoothing** : float, default=1e-9
  - **X** : array-like of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,)
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **X** : array-like of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,)
  - **classes** : array-like of shape (n_classes,), default=None
  - **sample_weight** : array-like of shape (n_samples,), default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **class_count_** : ndarray of shape (n_classes,)
  - **class_prior_** : ndarray of shape (n_classes,)
  - **classes_** : ndarray of shape (n_classes,)
  - **epsilon_** : float
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)
  - **var_** : ndarray of shape (n_classes, n_features)
  - **theta_** : ndarray of shape (n_classes, n_features)
  - **self** : ndarray of shape (n_classes, n_features)
  - **self** : object

  #### *List of methods:*
  - **fit(X, y[, sample_weight])** : Fit Gaussian Naive Bayes according to X, y.
  - **get_params([deep])** : Get parameters for this estimator.
  - **partial_fit(X, y[, classes, sample_weight])** : Incremental fit on a batch of samples.
  - **predict(X)** : Perform classification on an array of test vectors X.
  - **predict_log_proba(X)** : Return log-probability estimates for the test vector X.
  - **predict_proba(X)** : Return probability estimates for the test vector X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*BernoulliNB*](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.BernoulliNB.html)
  class sklearn.naive_bayes.BernoulliNB(*, alpha=1.0, binarize=0.0, fit_prior=True, class_prior=None)[source]¶

  #### *List of parameters:*
  - **alpha** : float, default=1.0
  - **binarize** : float or None, default=0.0
  - **fit_prior** : bool, default=True
  - **class_prior** : array-like of shape (n_classes,), default=None
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,)
  - **classes** : array-like of shape (n_classes,), default=None
  - **sample_weight** : array-like of shape (n_samples,), default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **class_count_** : ndarray of shape (n_classes,)
  - **class_log_prior_** : ndarray of shape (n_classes,)
  - **classes_** : ndarray of shape (n_classes,)
  - **feature_count_** : ndarray of shape (n_classes, n_features)
  - **feature_log_prob_** : ndarray of shape (n_classes, n_features)
  - **n_features_in_** : int
  - **feature_names_in_** : int
  - **self** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X, y[, sample_weight])** : Fit Naive Bayes classifier according to X, y.
  - **get_params([deep])** : Get parameters for this estimator.
  - **partial_fit(X, y[, classes, sample_weight])** : Incremental fit on a batch of samples.
  - **predict(X)** : Perform classification on an array of test vectors X.
  - **predict_log_proba(X)** : Return log-probability estimates for the test vector X.
  - **predict_proba(X)** : Return probability estimates for the test vector X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*ComplementNB*](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.ComplementNB.html)
  class sklearn.naive_bayes.ComplementNB(*, alpha=1.0, fit_prior=True, class_prior=None, norm=False)[source]¶

  #### *List of parameters:*
  - **alpha** : float, default=1.0
  - **fit_prior** : bool, default=True
  - **class_prior** : array-like of shape (n_classes,), default=None
  - **norm** : bool, default=False
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,)
  - **classes** : array-like of shape (n_classes,), default=None
  - **sample_weight** : array-like of shape (n_samples,), default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **class_count_** : ndarray of shape (n_classes,)
  - **class_log_prior_** : ndarray of shape (n_classes,)
  - **classes_** : ndarray of shape (n_classes,)
  - **feature_all_** : ndarray of shape (n_features,)
  - **feature_count_** : ndarray of shape (n_classes, n_features)
  - **feature_log_prob_** : ndarray of shape (n_classes, n_features)
  - **n_features_in_** : int
  - **feature_names_in_** : int
  - **self** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X, y[, sample_weight])** : Fit Naive Bayes classifier according to X, y.
  - **get_params([deep])** : Get parameters for this estimator.
  - **partial_fit(X, y[, classes, sample_weight])** : Incremental fit on a batch of samples.
  - **predict(X)** : Perform classification on an array of test vectors X.
  - **predict_log_proba(X)** : Return log-probability estimates for the test vector X.
  - **predict_proba(X)** : Return probability estimates for the test vector X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*DecisionTreeClassifier*](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html)
  class sklearn.tree.DecisionTreeClassifier(*, criterion='gini', splitter='best', max_depth=None, min_samples_split=2, min_samples_leaf=1, min_weight_fraction_leaf=0.0, max_features=None, random_state=None, max_leaf_nodes=None, min_impurity_decrease=0.0, class_weight=None, ccp_alpha=0.0)[source]¶

  #### *List of parameters:*
  - **criterion** : {“gini”, “entropy”, “log_loss”}, default=”gini”
  - **splitter** : {“best”, “random”}, default=”best”
  - **max_depth** : int, default=None
  - **min_samples_split** : int or float, default=2
  - **min_samples_leaf** : int or float, default=1
  - **min_weight_fraction_leaf** : float, default=0.0
  - **max_features** : int, float or {“auto”, “sqrt”, “log2”}, default=None
  - **random_state** : int, RandomState instance or None, default=None
  - **max_leaf_nodes** : int, default=None
  - **min_impurity_decrease** : float, default=0.0
  - **class_weight** : dict, list of dict or “balanced”, default=None
  - **ccp_alpha** : non-negative float, default=0.0
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,) or (n_samples, n_outputs)
  - **sample_weight** : array-like of shape (n_samples,), default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **classes_** : ndarray of shape (n_classes,) or list of ndarray
  - **max_features_** : ndarray of shape (n_features,)
  - **n_classes_** : int
  - **n_features_in_** : int or list of int
  - **feature_names_in_** : int
  - **n_outputs_** : int
  - **tree_** : ndarray of shape (n_features_in_,)
  - **ccp_path** : int

  #### *List of methods:*
  - **apply(X[, check_input])** : Return the index of the leaf that each sample is predicted as.
  - **cost_complexity_pruning_path(X, y[, ...])** : Compute the pruning path during Minimal Cost-Complexity Pruning.
  - **decision_path(X[, check_input])** : Return the decision path in the tree.
  - **fit(X, y[, sample_weight, check_input])** : Build a decision tree classifier from the training set (X, y).
  - **get_depth()** : Return the depth of the decision tree.
  - **get_n_leaves()** : Return the number of leaves of the decision tree.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X[, check_input])** : Predict class or regression value for X.
  - **predict_log_proba(X)** : Predict class log-probabilities of the input samples X.
  - **predict_proba(X[, check_input])** : Predict class probabilities of the input samples X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*DecisionTreeRegressor*](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeRegressor.html)
  class sklearn.tree.DecisionTreeRegressor(*, criterion='squared_error', splitter='best', max_depth=None, min_samples_split=2, min_samples_leaf=1, min_weight_fraction_leaf=0.0, max_features=None, random_state=None, max_leaf_nodes=None, min_impurity_decrease=0.0, ccp_alpha=0.0)[source]¶

  #### *List of parameters:*
  - **criterion** : {“squared_error”, “friedman_mse”, “absolute_error”,             “poisson”}, default=”squared_error”
  - **splitter** : {“best”, “random”}, default=”best”
  - **max_depth** : int, default=None
  - **min_samples_split** : int or float, default=2
  - **min_samples_leaf** : int or float, default=1
  - **min_weight_fraction_leaf** : float, default=0.0
  - **max_features** : int, float or {“auto”, “sqrt”, “log2”}, default=None
  - **random_state** : int, RandomState instance or None, default=None
  - **max_leaf_nodes** : int, default=None
  - **min_impurity_decrease** : float, default=0.0
  - **ccp_alpha** : non-negative float, default=0.0
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,) or (n_samples, n_outputs)
  - **sample_weight** : array-like of shape (n_samples,), default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **max_features_** : ndarray of shape (n_features,)
  - **n_features_in_** : int
  - **feature_names_in_** : int
  - **n_outputs_** : int
  - **tree_** : ndarray of shape (n_features_in_,)
  - **ccp_path** : int

  #### *List of methods:*
  - **apply(X[, check_input])** : Return the index of the leaf that each sample is predicted as.
  - **cost_complexity_pruning_path(X, y[, ...])** : Compute the pruning path during Minimal Cost-Complexity Pruning.
  - **decision_path(X[, check_input])** : Return the decision path in the tree.
  - **fit(X, y[, sample_weight, check_input])** : Build a decision tree regressor from the training set (X, y).
  - **get_depth()** : Return the depth of the decision tree.
  - **get_n_leaves()** : Return the number of leaves of the decision tree.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X[, check_input])** : Predict class or regression value for X.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*KNeighborsClassifier*](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)
  class sklearn.neighbors.KNeighborsClassifier(n_neighbors=5, *, weights='uniform', algorithm='auto', leaf_size=30, p=2, metric='minkowski', metric_params=None, n_jobs=None)[source]¶

  #### *List of parameters:*
  - **n_neighbors** : int, default=5
  - **weights** : {‘uniform’, ‘distance’} or callable, default=’uniform’
  - **algorithm** : {‘auto’, ‘ball_tree’, ‘kd_tree’, ‘brute’}, default=’auto’
  - **leaf_size** : int, default=30
  - **p** : int, default=2
  - **metric** : str or callable, default=’minkowski’
  - **metric_params** : dict, default=None
  - **n_jobs** : int, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **classes_** : array of shape (n_classes,)
  - **effective_metric_** : str or callble
  - **effective_metric_params_** : dict
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)
  - **n_samples_fit_** : int
  - **outputs_2d_** : bool

  #### *List of methods:*
  - **fit(X, y)** : Fit the k-nearest neighbors classifier from the training dataset.
  - **get_params([deep])** : Get parameters for this estimator.
  - **kneighbors([X, n_neighbors, return_distance])** : Find the K-neighbors of a point.
  - **kneighbors_graph([X, n_neighbors, mode])** : Compute the (weighted) graph of k-Neighbors for points in X.
  - **predict(X)** : Predict the class labels for the provided data.
  - **predict_proba(X)** : Return probability estimates for the test data X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*KMeans*](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html)
  class sklearn.cluster.KMeans(n_clusters=8, *, init='k-means++', n_init=10, max_iter=300, tol=0.0001, verbose=0, random_state=None, copy_x=True, algorithm='lloyd')[source]¶

  #### *List of parameters:*
  - **n_clusters** : int, default=8
  - **init** : {‘k-means++’, ‘random’}, callable or array-like of shape             (n_clusters, n_features), default=’k-means++’
  - **n_init** : int, default=10
  - **max_iter** : int, default=300
  - **tol** : float, default=1e-4
  - **verbose** : int, default=0
  - **random_state** : int, RandomState instance or None, default=None
  - **copy_x** : bool, default=True
  - **algorithm** : {“lloyd”, “elkan”, “auto”, “full”}, default=”lloyd”
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : Ignored
  - **sample_weight** : array-like of shape (n_samples,), default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **cluster_centers_** : ndarray of shape (n_clusters, n_features)
  - **labels_** : ndarray of shape (n_samples,)
  - **inertia_** : float
  - **n_iter_** : int
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)
  - **self** : object

  #### *List of methods:*
  - **fit(X[, y, sample_weight])** : Compute k-means clustering.
  - **fit_predict(X[, y, sample_weight])** : Compute cluster centers and predict cluster index for each sample.
  - **fit_transform(X[, y, sample_weight])** : Compute clustering and transform X to cluster-distance space.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X[, sample_weight])** : Predict the closest cluster each sample in X belongs to.
  - **score(X[, y, sample_weight])** : Opposite of the value of X on the K-means objective.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Transform X to a cluster-distance space.


## [*AgglomerativeClustering*](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html)
  class sklearn.cluster.AgglomerativeClustering(n_clusters=2, *, affinity='euclidean', memory=None, connectivity=None, compute_full_tree='auto', linkage='ward', distance_threshold=None, compute_distances=False)[source]¶

  #### *List of parameters:*
  - **n_clusters** : int or None, default=2
  - **affinity** : str or callable, default=’euclidean’
  - **memory** : str or object with the joblib.Memory interface, default=None
  - **connectivity** : array-like or callable, default=None
  - **compute_full_tree** : ‘auto’ or bool, default=’auto’
  - **linkage** : {‘ward’, ‘complete’, ‘average’, ‘single’}, default=’ward’
  - **distance_threshold** : float, default=None
  - **compute_distances** : bool, default=False

  #### *List of attributes:*

  #### *List of attributes:*
  - **n_clusters_** : int
  - **labels_** : ndarray of shape (n_samples)
  - **n_leaves_** : int
  - **n_connected_components_** : int
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)
  - **children_** : array-like of shape (n_samples-1, 2)
  - **distances_** : array-like of shape (n_nodes-1,)

  #### *List of methods:*
  - **fit(X[, y])** : Fit the hierarchical clustering from features, or distance matrix.
  - **fit_predict(X[, y])** : Fit and return the result of each sample's clustering assignment.
  - **get_params([deep])** : Get parameters for this estimator.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*RandomForestClassifier*](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
  class sklearn.ensemble.RandomForestClassifier(n_estimators=100, *, criterion='gini', max_depth=None, min_samples_split=2, min_samples_leaf=1, min_weight_fraction_leaf=0.0, max_features='sqrt', max_leaf_nodes=None, min_impurity_decrease=0.0, bootstrap=True, oob_score=False, n_jobs=None, random_state=None, verbose=0, warm_start=False, class_weight=None, ccp_alpha=0.0, max_samples=None)[source]¶

  #### *List of parameters:*
  - **n_estimators** : int, default=100
  - **criterion** : {“gini”, “entropy”, “log_loss”}, default=”gini”
  - **max_depth** : int, default=None
  - **min_samples_split** : int or float, default=2
  - **min_samples_leaf** : int or float, default=1
  - **min_weight_fraction_leaf** : float, default=0.0
  - **max_features** : {“sqrt”, “log2”, None}, int or float, default=”sqrt”
  - **max_leaf_nodes** : int, default=None
  - **min_impurity_decrease** : float, default=0.0
  - **bootstrap** : bool, default=True
  - **oob_score** : bool, default=False
  - **n_jobs** : int, default=None
  - **random_state** : int, RandomState instance or None, default=None
  - **verbose** : int, default=0
  - **warm_start** : bool, default=False
  - **class_weight** : {“balanced”, “balanced_subsample”}, dict or list of dicts,             default=None
  - **ccp_alpha** : non-negative float, default=0.0
  - **max_samples** : int or float, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **base_estimator_** : DecisionTreeClassifier
  - **estimators_** : list of DecisionTreeClassifier
  - **classes_** : ndarray of shape (n_classes,) or a list of such arrays
  - **n_classes_** : int or list
  - **n_features_in_** : int
  - **feature_names_in_** : int
  - **n_outputs_** : ndarray of shape (n_features_in_,)
  - **oob_score_** : int
  - **oob_decision_function_** : ndarray of shape (n_features,)

  #### *List of methods:*
  - **apply(X)** : Apply trees in the forest to X, return leaf indices.
  - **decision_path(X)** : Return the decision path in the forest.
  - **fit(X, y[, sample_weight])** : Build a forest of trees from the training set (X, y).
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict class for X.
  - **predict_log_proba(X)** : Predict class log-probabilities for X.
  - **predict_proba(X)** : Predict class probabilities for X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*RandomForestRegressor*](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html)
  class sklearn.ensemble.RandomForestRegressor(n_estimators=100, *, criterion='squared_error', max_depth=None, min_samples_split=2, min_samples_leaf=1, min_weight_fraction_leaf=0.0, max_features=1.0, max_leaf_nodes=None, min_impurity_decrease=0.0, bootstrap=True, oob_score=False, n_jobs=None, random_state=None, verbose=0, warm_start=False, ccp_alpha=0.0, max_samples=None)[source]¶

  #### *List of parameters:*
  - **n_estimators** : int, default=100
  - **criterion** : {“squared_error”, “absolute_error”, “poisson”},             default=”squared_error”
  - **max_depth** : int, default=None
  - **min_samples_split** : int or float, default=2
  - **min_samples_leaf** : int or float, default=1
  - **min_weight_fraction_leaf** : float, default=0.0
  - **max_features** : {“sqrt”, “log2”, None}, int or float, default=1.0
  - **max_leaf_nodes** : int, default=None
  - **min_impurity_decrease** : float, default=0.0
  - **bootstrap** : bool, default=True
  - **oob_score** : bool, default=False
  - **n_jobs** : int, default=None
  - **random_state** : int, RandomState instance or None, default=None
  - **verbose** : int, default=0
  - **warm_start** : bool, default=False
  - **ccp_alpha** : non-negative float, default=0.0
  - **max_samples** : int or float, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **base_estimator_** : DecisionTreeRegressor
  - **estimators_** : list of DecisionTreeRegressor
  - **n_features_in_** : ndarray of shape (n_features,)
  - **feature_names_in_** : int
  - **n_outputs_** : int
  - **oob_score_** : ndarray of shape (n_features_in_,)
  - **oob_prediction_** : int

  #### *List of methods:*
  - **apply(X)** : Apply trees in the forest to X, return leaf indices.
  - **decision_path(X)** : Return the decision path in the forest.
  - **fit(X, y[, sample_weight])** : Build a forest of trees from the training set (X, y).
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict regression target for X.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*AdaBoostClassifier*](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.AdaBoostClassifier.html)
  class sklearn.ensemble.AdaBoostClassifier(base_estimator=None, *, n_estimators=50, learning_rate=1.0, algorithm='SAMME.R', random_state=None)[source]¶

  #### *List of parameters:*
  - **base_estimator** : object, default=None
  - **n_estimators** : int, default=50
  - **learning_rate** : float, default=1.0
  - **algorithm** : {‘SAMME’, ‘SAMME.R’}, default=’SAMME.R’
  - **random_state** : int, RandomState instance or None, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **base_estimator_** : estimator
  - **estimators_** : list of classifiers
  - **classes_** : ndarray of shape (n_classes,)
  - **n_classes_** : int
  - **estimator_weights_** : ndarray of floats
  - **estimator_errors_** : ndarray of floats
  - **n_features_in_** : ndarray of shape (n_features,)
  - **feature_names_in_** : int

  #### *List of methods:*
  - **decision_function(X)** : Compute the decision function of X.
  - **fit(X, y[, sample_weight])** : Build a boosted classifier from the training set (X, y).
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict classes for X.
  - **predict_log_proba(X)** : Predict class log-probabilities for X.
  - **predict_proba(X)** : Predict class probabilities for X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **staged_decision_function(X)** : Compute decision function of X for each boosting iteration.
  - **staged_predict(X)** : Return staged predictions for X.
  - **staged_predict_proba(X)** : Predict class probabilities for X.
  - **staged_score(X, y[, sample_weight])** : Return staged scores for X, y.


## [*AdaBoostRegressor*](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.AdaBoostRegressor.html)
  class sklearn.ensemble.AdaBoostRegressor(base_estimator=None, *, n_estimators=50, learning_rate=1.0, loss='linear', random_state=None)[source]¶

  #### *List of parameters:*
  - **base_estimator** : object, default=None
  - **n_estimators** : int, default=50
  - **learning_rate** : float, default=1.0
  - **loss** : {‘linear’, ‘square’, ‘exponential’}, default=’linear’
  - **random_state** : int, RandomState instance or None, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **base_estimator_** : estimator
  - **estimators_** : list of regressors
  - **estimator_weights_** : ndarray of floats
  - **estimator_errors_** : ndarray of floats
  - **n_features_in_** : ndarray of shape (n_features,)
  - **feature_names_in_** : int

  #### *List of methods:*
  - **fit(X, y[, sample_weight])** : Build a boosted regressor from the training set (X, y).
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict regression value for X.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **staged_predict(X)** : Return staged predictions for X.
  - **staged_score(X, y[, sample_weight])** : Return staged scores for X, y.


## [*BaggingClassifier*](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.BaggingClassifier.html)
  class sklearn.ensemble.BaggingClassifier(base_estimator=None, n_estimators=10, *, max_samples=1.0, max_features=1.0, bootstrap=True, bootstrap_features=False, oob_score=False, warm_start=False, n_jobs=None, random_state=None, verbose=0)[source]¶

  #### *List of parameters:*
  - **base_estimator** : object, default=None
  - **n_estimators** : int, default=10
  - **max_samples** : int or float, default=1.0
  - **max_features** : int or float, default=1.0
  - **bootstrap** : bool, default=True
  - **bootstrap_features** : bool, default=False
  - **oob_score** : bool, default=False
  - **warm_start** : bool, default=False
  - **n_jobs** : int, default=None
  - **random_state** : int, RandomState instance or None, default=None
  - **verbose** : int, default=0

  #### *List of attributes:*

  #### *List of attributes:*
  - **base_estimator_** : estimator
  - **n_features_in_** : int
  - **feature_names_in_** : int
  - **estimators_** : ndarray of shape (n_features_in_,)
  - **estimators_features_** : list of estimators
  - **classes_** : list of arrays
  - **n_classes_** : list of arrays
  - **oob_score_** : ndarray of shape (n_classes,)
  - **oob_decision_function_** : int or list

  #### *List of methods:*
  - **decision_function(X)** : Average of the decision functions of the base classifiers.
  - **fit(X, y[, sample_weight])** : Build a Bagging ensemble of estimators from the training set (X, y).
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict class for X.
  - **predict_log_proba(X)** : Predict class log-probabilities for X.
  - **predict_proba(X)** : Predict class probabilities for X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*BaggingRegressor*](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.BaggingRegressor.html)
  class sklearn.ensemble.BaggingRegressor(base_estimator=None, n_estimators=10, *, max_samples=1.0, max_features=1.0, bootstrap=True, bootstrap_features=False, oob_score=False, warm_start=False, n_jobs=None, random_state=None, verbose=0)[source]¶

  #### *List of parameters:*
  - **base_estimator** : object, default=None
  - **n_estimators** : int, default=10
  - **max_samples** : int or float, default=1.0
  - **max_features** : int or float, default=1.0
  - **bootstrap** : bool, default=True
  - **bootstrap_features** : bool, default=False
  - **oob_score** : bool, default=False
  - **warm_start** : bool, default=False
  - **n_jobs** : int, default=None
  - **random_state** : int, RandomState instance or None, default=None
  - **verbose** : int, default=0

  #### *List of attributes:*

  #### *List of attributes:*
  - **base_estimator_** : estimator
  - **n_features_in_** : int
  - **feature_names_in_** : int
  - **estimators_** : ndarray of shape (n_features_in_,)
  - **estimators_features_** : list of estimators
  - **oob_score_** : list of arrays
  - **oob_prediction_** : list of arrays

  #### *List of methods:*
  - **fit(X, y[, sample_weight])** : Build a Bagging ensemble of estimators from the training set (X, y).
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict regression target for X.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*GradientBoostingClassifier*](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html)
  class sklearn.ensemble.GradientBoostingClassifier(*, loss='log_loss', learning_rate=0.1, n_estimators=100, subsample=1.0, criterion='friedman_mse', min_samples_split=2, min_samples_leaf=1, min_weight_fraction_leaf=0.0, max_depth=3, min_impurity_decrease=0.0, init=None, random_state=None, max_features=None, verbose=0, max_leaf_nodes=None, warm_start=False, validation_fraction=0.1, n_iter_no_change=None, tol=0.0001, ccp_alpha=0.0)[source]¶

  #### *List of parameters:*
  - **loss** : {‘log_loss’, ‘deviance’, ‘exponential’}, default=’log_loss’
  - **learning_rate** : float, default=0.1
  - **n_estimators** : int, default=100
  - **subsample** : float, default=1.0
  - **criterion** : {‘friedman_mse’, ‘squared_error’, ‘mse’},             default=’friedman_mse’
  - **min_samples_split** : int or float, default=2
  - **min_samples_leaf** : int or float, default=1
  - **min_weight_fraction_leaf** : float, default=0.0
  - **max_depth** : int, default=3
  - **min_impurity_decrease** : float, default=0.0
  - **init** : estimator or ‘zero’, default=None
  - **random_state** : int, RandomState instance or None, default=None
  - **max_features** : {‘auto’, ‘sqrt’, ‘log2’}, int or float, default=None
  - **verbose** : int, default=0
  - **max_leaf_nodes** : int, default=None
  - **warm_start** : bool, default=False
  - **validation_fraction** : float, default=0.1
  - **n_iter_no_change** : int, default=None
  - **tol** : float, default=1e-4
  - **ccp_alpha** : non-negative float, default=0.0

  #### *List of attributes:*

  #### *List of attributes:*
  - **n_estimators_** : int
  - **oob_improvement_** : ndarray of shape (n_features,)
  - **train_score_** : ndarray of shape (n_estimators,)
  - **init_** : ndarray of shape (n_estimators,)
  - **estimators_** : LossFunction
  - **classes_** : estimator
  - **n_features_in_** : ndarray of DecisionTreeRegressor of             shape (n_estimators, loss_.K)
  - **feature_names_in_** : ndarray of shape (n_classes,)
  - **n_classes_** : int
  - **max_features_** : int

  #### *List of methods:*
  - **apply(X)** : Apply trees in the ensemble to X, return leaf indices.
  - **decision_function(X)** : Compute the decision function of X.
  - **fit(X, y[, sample_weight, monitor])** : Fit the gradient boosting model.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict class for X.
  - **predict_log_proba(X)** : Predict class log-probabilities for X.
  - **predict_proba(X)** : Predict class probabilities for X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **staged_decision_function(X)** : Compute decision function of X for each iteration.
  - **staged_predict(X)** : Predict class at each stage for X.
  - **staged_predict_proba(X)** : Predict class probabilities at each stage for X.


## [*GradientBoostingRegressor*](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingRegressor.html)
  class sklearn.ensemble.GradientBoostingRegressor(*, loss='squared_error', learning_rate=0.1, n_estimators=100, subsample=1.0, criterion='friedman_mse', min_samples_split=2, min_samples_leaf=1, min_weight_fraction_leaf=0.0, max_depth=3, min_impurity_decrease=0.0, init=None, random_state=None, max_features=None, alpha=0.9, verbose=0, max_leaf_nodes=None, warm_start=False, validation_fraction=0.1, n_iter_no_change=None, tol=0.0001, ccp_alpha=0.0)[source]¶

  #### *List of parameters:*
  - **loss** : {‘squared_error’, ‘absolute_error’, ‘huber’, ‘quantile’},             default=’squared_error’
  - **learning_rate** : float, default=0.1
  - **n_estimators** : int, default=100
  - **subsample** : float, default=1.0
  - **criterion** : {‘friedman_mse’, ‘squared_error’, ‘mse’},             default=’friedman_mse’
  - **min_samples_split** : int or float, default=2
  - **min_samples_leaf** : int or float, default=1
  - **min_weight_fraction_leaf** : float, default=0.0
  - **max_depth** : int, default=3
  - **min_impurity_decrease** : float, default=0.0
  - **init** : estimator or ‘zero’, default=None
  - **random_state** : int, RandomState instance or None, default=None
  - **max_features** : {‘auto’, ‘sqrt’, ‘log2’}, int or float, default=None
  - **alpha** : float, default=0.9
  - **verbose** : int, default=0
  - **max_leaf_nodes** : int, default=None
  - **warm_start** : bool, default=False
  - **validation_fraction** : float, default=0.1
  - **n_iter_no_change** : int, default=None
  - **tol** : float, default=1e-4
  - **ccp_alpha** : non-negative float, default=0.0

  #### *List of attributes:*

  #### *List of attributes:*
  - **oob_improvement_** : ndarray of shape (n_features,)
  - **train_score_** : ndarray of shape (n_estimators,)
  - **init_** : ndarray of shape (n_estimators,)
  - **estimators_** : LossFunction
  - **n_estimators_** : estimator
  - **n_features_in_** : ndarray of DecisionTreeRegressor of shape (n_estimators, 1)
  - **feature_names_in_** : int
  - **max_features_** : int

  #### *List of methods:*
  - **apply(X)** : Apply trees in the ensemble to X, return leaf indices.
  - **fit(X, y[, sample_weight, monitor])** : Fit the gradient boosting model.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Predict regression target for X.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **staged_predict(X)** : Predict regression target at each stage for X.


## [*MLPClassifier*](https://scikit-learn.org/stable/modules/generated/sklearn.neural_network.MLPClassifier.html)
  class sklearn.neural_network.MLPClassifier(hidden_layer_sizes=(100,), activation='relu', *, solver='adam', alpha=0.0001, batch_size='auto', learning_rate='constant', learning_rate_init=0.001, power_t=0.5, max_iter=200, shuffle=True, random_state=None, tol=0.0001, verbose=False, warm_start=False, momentum=0.9, nesterovs_momentum=True, early_stopping=False, validation_fraction=0.1, beta_1=0.9, beta_2=0.999, epsilon=1e-08, n_iter_no_change=10, max_fun=15000)[source]¶

  #### *List of parameters:*
  - **hidden_layer_sizes** : tuple, length = n_layers - 2, default=(100,)
  - **activation** : {‘identity’, ‘logistic’, ‘tanh’, ‘relu’}, default=’relu’
  - **solver** : {‘lbfgs’, ‘sgd’, ‘adam’}, default=’adam’
  - **alpha** : float, default=0.0001
  - **batch_size** : int, default=’auto’
  - **learning_rate** : {‘constant’, ‘invscaling’, ‘adaptive’}, default=’constant’
  - **learning_rate_init** : float, default=0.001
  - **power_t** : float, default=0.5
  - **max_iter** : int, default=200
  - **shuffle** : bool, default=True
  - **random_state** : int, RandomState instance, default=None
  - **tol** : float, default=1e-4
  - **verbose** : bool, default=False
  - **warm_start** : bool, default=False
  - **momentum** : float, default=0.9
  - **nesterovs_momentum** : bool, default=True
  - **early_stopping** : bool, default=False
  - **validation_fraction** : float, default=0.1
  - **beta_1** : float, default=0.9
  - **beta_2** : float, default=0.999
  - **epsilon** : float, default=1e-8
  - **n_iter_no_change** : int, default=10
  - **max_fun** : int, default=15000

  #### *List of attributes:*

  #### *List of attributes:*
  - **classes_** : ndarray or list of ndarray of shape (n_classes,)
  - **loss_** : float
  - **best_loss_** : float
  - **loss_curve_** : list of shape (n_iter_,)
  - **t_** : int
  - **coefs_** : list of shape (n_layers - 1,)
  - **intercepts_** : list of shape (n_layers - 1,)
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)
  - **n_iter_** : int
  - **n_layers_** : int
  - **n_outputs_** : int
  - **out_activation_** : str

  #### *List of methods:*
  - **fit(X, y)** : Fit the model to data matrix X and target(s) y.
  - **get_params([deep])** : Get parameters for this estimator.
  - **partial_fit(X, y[, classes])** : Update the model with a single iteration over the given data.
  - **predict(X)** : Predict using the multi-layer perceptron classifier.
  - **predict_log_proba(X)** : Return the log of probability estimates.
  - **predict_proba(X)** : Probability estimates.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*DummyRegressor*](https://scikit-learn.org/stable/modules/generated/sklearn.dummy.DummyRegressor.html)
  class sklearn.dummy.DummyRegressor(*, strategy='mean', constant=None, quantile=None)[source]¶

  #### *List of parameters:*
  - **strategy** : {“mean”, “median”, “quantile”, “constant”}, default=”mean”
  - **constant** : int or float or array-like of shape (n_outputs,), default=None
  - **quantile** : float in [0.0, 1.0], default=None
  - **X** : array-like of shape (n_samples, n_features)
  - **return_std** : bool, default=False

  #### *List of attributes:*

  #### *List of attributes:*
  - **constant_** : ndarray of shape (1, n_outputs)
  - **n_outputs_** : None
  - **y** : int
  - **y_std** : array-like of shape (n_samples,) or (n_samples, n_outputs)

  #### *List of methods:*
  - **fit(X, y[, sample_weight])** : Fit the random regressor.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X[, return_std])** : Perform classification on test vectors X.
  - **score(X, y[, sample_weight])** : Return the coefficient of determination R^2 of the prediction.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*DummyClassifier*](https://scikit-learn.org/stable/modules/generated/sklearn.dummy.DummyClassifier.html)
  class sklearn.dummy.DummyClassifier(*, strategy='prior', random_state=None, constant=None)[source]¶

  #### *List of parameters:*
  - **strategy** : {“most_frequent”, “prior”, “stratified”, “uniform”,             “constant”}, default=”prior”
  - **random_state** : int, RandomState instance or None, default=None
  - **constant** : int or str or array-like of shape (n_outputs,), default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **classes_** : ndarray of shape (n_classes,) or list of such arrays
  - **n_classes_** : int or list of int
  - **class_prior_** : ndarray of shape (n_classes,) or list of such arrays
  - **n_outputs_** : int
  - **sparse_output_** : None

  #### *List of methods:*
  - **fit(X, y[, sample_weight])** : Fit the baseline classifier.
  - **get_params([deep])** : Get parameters for this estimator.
  - **predict(X)** : Perform classification on test vectors X.
  - **predict_log_proba(X)** : Return log probability estimates for the test vectors X.
  - **predict_proba(X)** : Return probability estimates for the test vectors X.
  - **score(X, y[, sample_weight])** : Return the mean accuracy on the given test data and labels.
  - **set_params(\*\*params)** : Set the parameters of this estimator.


## [*load_iris*](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_iris.html)
  sklearn.datasets.load_iris(*, return_X_y=False, as_frame=False)[source]¶

  #### *List of parameters:*
  - **return_X_y** : bool, default=False
  - **as_frame** : bool, default=False

  #### *List of return values:*

  #### *List of attributes:*
  - **data** : Bunch
  - **(data, target)** : tuple if return_X_y is True

  #### *List of methods:*
  - **Classes** : 3
  - **Samples per class** : 50
  - **Samples total** : 150
  - **Dimensionality** : 4
  - **Features** : real, positive


## [*fetch_california_housing*](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html)
  sklearn.datasets.fetch_california_housing(*, data_home=None, download_if_missing=True, return_X_y=False, as_frame=False)[source]¶

  #### *List of parameters:*
  - **data_home** : str, default=None
  - **download_if_missing** : bool, default=True
  - **return_X_y** : bool, default=False
  - **as_frame** : bool, default=False

  #### *List of return values:*

  #### *List of attributes:*
  - **dataset** : Bunch
  - **(data, target)** : tuple if return_X_y is True

  #### *List of methods:*
  - **Samples total** : 20640
  - **Dimensionality** : 8
  - **Features** : real
  - **Target** : real 0.15 - 5.


## [*fetch_openml*](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_openml.html)
  sklearn.datasets.fetch_openml(name: Optional[str] = None, *, version: Union[str, int] = 'active', data_id: Optional[int] = None, data_home: Optional[str] = None, target_column: Optional[Union[str, List]] = 'default-target', cache: bool = True, return_X_y: bool = False, as_frame: Union[str, bool] = 'auto', n_retries: int = 3, delay: float = 1.0)[source]¶

  #### *List of parameters:*
  - **name** : str, default=None
  - **version** : int or ‘active’, default=’active’
  - **data_id** : int, default=None
  - **data_home** : str, default=None
  - **target_column** : str, list or None, default=’default-target’
  - **cache** : bool, default=True
  - **return_X_y** : bool, default=False
  - **as_frame** : bool or ‘auto’, default=’auto’
  - **n_retries** : int, default=3
  - **delay** : float, default=1.0

  #### *List of return values:*

  #### *List of attributes:*
  - **data** : Bunch
  - **(data, target)** : tuple if return_X_y is True

  #### *List of methods:*


## [*make_blobs*](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.make_blobs.html)
  sklearn.datasets.make_blobs(n_samples=100, n_features=2, *, centers=None, cluster_std=1.0, center_box=(- 10.0, 10.0), shuffle=True, random_state=None, return_centers=False)[source]¶

  #### *List of parameters:*
  - **n_samples** : int or array-like, default=100
  - **n_features** : int, default=2
  - **centers** : int or ndarray of shape (n_centers, n_features), default=None
  - **cluster_std** : float or array-like of float, default=1.0
  - **center_box** : tuple of float (min, max), default=(-10.0, 10.0)
  - **shuffle** : bool, default=True
  - **random_state** : int, RandomState instance or None, default=None
  - **return_centers** : bool, default=False

  #### *List of return values:*

  #### *List of attributes:*
  - **X** : ndarray of shape (n_samples, n_features)
  - **y** : ndarray of shape (n_samples,)
  - **centers** : ndarray of shape (n_centers, n_features)

  #### *List of methods:*


## [*make_multilabel_classification*](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.make_multilabel_classification.html)
  sklearn.datasets.make_multilabel_classification(n_samples=100, n_features=20, *, n_classes=5, n_labels=2, length=50, allow_unlabeled=True, sparse=False, return_indicator='dense', return_distributions=False, random_state=None)[source]¶

  #### *List of parameters:*
  - **n_samples** : int, default=100
  - **n_features** : int, default=20
  - **n_classes** : int, default=5
  - **n_labels** : int, default=2
  - **length** : int, default=50
  - **allow_unlabeled** : bool, default=True
  - **sparse** : bool, default=False
  - **return_indicator** : {‘dense’, ‘sparse’} or False, default=’dense’
  - **return_distributions** : bool, default=False
  - **random_state** : int, RandomState instance or None, default=None

  #### *List of return values:*

  #### *List of attributes:*
  - **X** : ndarray of shape (n_samples, n_features)
  - **Y** : {ndarray, sparse matrix} of shape (n_samples, n_classes)
  - **p_c** : ndarray of shape (n_classes,)
  - **p_w_c** : ndarray of shape (n_features, n_classes)

  #### *List of methods:*


## [*train_test_split*](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html)
  sklearn.model_selection.train_test_split(*arrays, test_size=None, train_size=None, random_state=None, shuffle=True, stratify=None)[source]¶

  #### *List of parameters:*
  - ***arrays** : sequence of indexables with same length / shape[0]
  - **test_size** : float or int, default=None
  - **train_size** : float or int, default=None
  - **random_state** : int, RandomState instance or None, default=None
  - **shuffle** : bool, default=True
  - **stratify** : array-like, default=None

  #### *List of return values:*

  #### *List of attributes:*
  - **splitting** : list, length=2 * len(arrays)

  #### *List of methods:*


## [*cross_validate*](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.cross_validate.html)
  sklearn.model_selection.cross_validate(estimator, X, y=None, *, groups=None, scoring=None, cv=None, n_jobs=None, verbose=0, fit_params=None, pre_dispatch='2*n_jobs', return_train_score=False, return_estimator=False, error_score=nan)[source]¶

  #### *List of parameters:*
  - **estimator** : estimator object implementing ‘fit’
  - **X** : array-like of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,) or (n_samples, n_outputs), default=None
  - **groups** : array-like of shape (n_samples,), default=None
  - **scoring** : str, callable, list, tuple, or dict, default=None
  - **cv** : int, cross-validation generator or an iterable, default=None
  - **n_jobs** : int, default=None
  - **verbose** : int, default=0
  - **fit_params** : dict, default=None
  - **pre_dispatch** : int or str, default=’2*n_jobs’
  - **return_train_score** : bool, default=False
  - **return_estimator** : bool, default=False
  - **error_score** : ‘raise’ or numeric, default=np.nan

  #### *List of return values:*

  #### *List of attributes:*
  - **scores** : dict of float arrays of shape (n_splits,)

  #### *List of methods:*


## [*cross_val_score*](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.cross_val_score.html)
  sklearn.model_selection.cross_val_score(estimator, X, y=None, *, groups=None, scoring=None, cv=None, n_jobs=None, verbose=0, fit_params=None, pre_dispatch='2*n_jobs', error_score=nan)[source]¶

  #### *List of parameters:*
  - **estimator** : estimator object implementing ‘fit’
  - **X** : array-like of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,) or (n_samples, n_outputs),             default=None
  - **groups** : array-like of shape (n_samples,), default=None
  - **scoring** : str or callable, default=None
  - **cv** : int, cross-validation generator or an iterable, default=None
  - **n_jobs** : int, default=None
  - **verbose** : int, default=0
  - **fit_params** : dict, default=None
  - **pre_dispatch** : int or str, default=’2*n_jobs’
  - **error_score** : ‘raise’ or numeric, default=np.nan

  #### *List of return values:*

  #### *List of attributes:*
  - **scores** : ndarray of float of shape=(len(list(cv)),)

  #### *List of methods:*


## [*cross_val_predict*](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.cross_val_predict.html)
  sklearn.model_selection.cross_val_predict(estimator, X, y=None, *, groups=None, cv=None, n_jobs=None, verbose=0, fit_params=None, pre_dispatch='2*n_jobs', method='predict')[source]¶

  #### *List of parameters:*
  - **estimator** : estimator object implementing ‘fit’ and ‘predict’
  - **X** : array-like of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,) or (n_samples, n_outputs),             default=None
  - **groups** : array-like of shape (n_samples,), default=None
  - **cv** : int, cross-validation generator or an iterable, default=None
  - **n_jobs** : int, default=None
  - **verbose** : int, default=0
  - **fit_params** : dict, default=None
  - **pre_dispatch** : int or str, default=’2*n_jobs’
  - **method** : {‘predict’, ‘predict_proba’, ‘predict_log_proba’,               ‘decision_function’}, default=’predict’

  #### *List of return values:*

  #### *List of attributes:*
  - **predictions** : ndarray

  #### *List of methods:*


## [*learning_curve*](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.learning_curve.html)
  sklearn.model_selection.learning_curve(estimator, X, y, *, groups=None, train_sizes=array([0.1, 0.33, 0.55, 0.78, 1.]), cv=None, scoring=None, exploit_incremental_learning=False, n_jobs=None, pre_dispatch='all', verbose=0, shuffle=False, random_state=None, error_score=nan, return_times=False, fit_params=None)[source]¶

  #### *List of parameters:*
  - **estimator** : object type that implements the “fit” and “predict” methods
  - **X** : array-like of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,) or (n_samples, n_outputs)
  - **groups** : array-like of  shape (n_samples,), default=None
  - **train_sizes** : array-like of shape (n_ticks,),             default=np.linspace(0.1, 1.0, 5)
  - **cv** : int, cross-validation generator or an iterable, default=None
  - **scoring** : str or callable, default=None
  - **exploit_incremental_learning** : bool, default=False
  - **n_jobs** : int, default=None
  - **pre_dispatch** : int or str, default=’all’
  - **verbose** : int, default=0
  - **shuffle** : bool, default=False
  - **random_state** : int, RandomState instance or None, default=None
  - **error_score** : ‘raise’ or numeric, default=np.nan
  - **return_times** : bool, default=False
  - **fit_params** : dict, default=None

  #### *List of return values:*

  #### *List of attributes:*
  - **train_sizes_abs** : array of shape (n_unique_ticks,)
  - **train_scores** : array of shape (n_ticks, n_cv_folds)
  - **test_scores** : array of shape (n_ticks, n_cv_folds)
  - **fit_times** : array of shape (n_ticks, n_cv_folds)
  - **score_times** : array of shape (n_ticks, n_cv_folds)

  #### *List of methods:*


## [*validation_curve*](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.validation_curve.html)
  sklearn.model_selection.validation_curve(estimator, X, y, *, param_name, param_range, groups=None, cv=None, scoring=None, n_jobs=None, pre_dispatch='all', verbose=0, error_score=nan, fit_params=None)[source]¶

  #### *List of parameters:*
  - **estimator** : object type that implements the “fit” and “predict” methods
  - **X** : array-like of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,) or (n_samples, n_outputs) or None
  - **param_name** : str
  - **param_range** : array-like of shape (n_values,)
  - **groups** : array-like of shape (n_samples,), default=None
  - **cv** : int, cross-validation generator or an iterable, default=None
  - **scoring** : str or callable, default=None
  - **n_jobs** : int, default=None
  - **pre_dispatch** : int or str, default=’all’
  - **verbose** : int, default=0
  - **fit_params** : dict, default=None
  - **error_score** : ‘raise’ or numeric, default=np.nan

  #### *List of return values:*

  #### *List of attributes:*
  - **train_scores** : array of shape (n_ticks, n_cv_folds)
  - **test_scores** : array of shape (n_ticks, n_cv_folds)

  #### *List of methods:*


## [*StratifiedShuffleSplit*](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.StratifiedShuffleSplit.html)
  class sklearn.model_selection.StratifiedShuffleSplit(n_splits=10, *, test_size=None, train_size=None, random_state=None)[source]¶

  #### *List of parameters:*
  - **X** : array-like of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,) or (n_samples, n_labels)
  - **groups** : object

  #### *List of attributes:*

  #### *List of attributes:*
  - **train** : ndarray
  - **test** : ndarray

  #### *List of methods:*
  - **get_n_splits([X, y, groups])** : Returns the number of splitting iterations in the cross-validator
  - **split(X, y[, groups])** : Generate indices to split data into training and test set.


## [*permutation_test_score*](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.permutation_test_score.html)
  sklearn.model_selection.permutation_test_score(estimator, X, y, *, groups=None, cv=None, n_permutations=100, n_jobs=None, random_state=0, verbose=0, scoring=None, fit_params=None)[source]¶

  #### *List of parameters:*
  - **estimator** : estimator object implementing ‘fit’
  - **X** : array-like of shape at least 2D
  - **y** : array-like of shape (n_samples,) or (n_samples, n_outputs) or None
  - **groups** : array-like of shape (n_samples,), default=None
  - **scoring** : str or callable, default=None
  - **cv** : int, cross-validation generator or an iterable, default=None
  - **n_permutations** : int, default=100
  - **n_jobs** : int, default=None
  - **random_state** : int, RandomState instance or None, default=0
  - **verbose** : int, default=0
  - **fit_params** : dict, default=None

  #### *List of return values:*

  #### *List of attributes:*
  - **score** : float
  - **permutation_scores** : array of shape (n_permutations,)
  - **pvalue** : float

  #### *List of methods:*


## [*GridSearchCV*](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html)
  class sklearn.model_selection.GridSearchCV(estimator, param_grid, *, scoring=None, n_jobs=None, refit=True, cv=None, verbose=0, pre_dispatch='2*n_jobs', error_score=nan, return_train_score=False)[source]¶

  #### *List of parameters:*
  - **estimator** : estimator object
  - **param_grid** : dict or list of dictionaries
  - **scoring** : str, callable, list, tuple or dict, default=None
  - **n_jobs** : int, default=None
  - **refit** : bool, str, or callable, default=True
  - **cv** : int, cross-validation generator or an iterable, default=None
  - **verbose** : int
  - **pre_dispatch** : int, or str, default=’2*n_jobs’
  - **error_score** : ‘raise’ or numeric, default=np.nan
  - **return_train_score** : bool, default=False
  - **X** : array-like of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples, n_output)             or (n_samples,), default=None
  - **groups** : array-like of shape (n_samples,), default=None
  - ****fit_params** : dict of str -> object

  #### *List of attributes:*

  #### *List of attributes:*
  - **cv_results_** : dict of numpy (masked) ndarrays
  - **best_estimator_** : estimator
  - **best_score_** : float
  - **best_params_** : dict
  - **best_index_** : int
  - **scorer_** : function or a dict
  - **n_splits_** : int
  - **refit_time_** : float
  - **multimetric_** : bool
  - **feature_names_in_** : ndarray of shape (n_classes,)
  - **self** : int

  #### *List of methods:*
  - **‘poly’** : –
  - **‘poly’** : –
  - **‘rbf’** : 0.1
  - **‘rbf’** : 0.2
  - **decision_function(X)** : Call decision_function on the estimator with the best found parameters.
  - **fit(X[, y, groups])** : Run fit with all sets of parameters.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(Xt)** : Call inverse_transform on the estimator with the best found params.
  - **predict(X)** : Call predict on the estimator with the best found parameters.
  - **predict_log_proba(X)** : Call predict_log_proba on the estimator with the best found parameters.
  - **predict_proba(X)** : Call predict_proba on the estimator with the best found parameters.
  - **score(X[, y])** : Return the score on the given data, if the estimator has been refit.
  - **score_samples(X)** : Call score_samples on the estimator with the best found parameters.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Call transform on the estimator with the best found parameters.


## [*RandomizedSearchCV*](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.RandomizedSearchCV.html)
  class sklearn.model_selection.RandomizedSearchCV(estimator, param_distributions, *, n_iter=10, scoring=None, n_jobs=None, refit=True, cv=None, verbose=0, pre_dispatch='2*n_jobs', random_state=None, error_score=nan, return_train_score=False)[source]¶

  #### *List of parameters:*
  - **estimator** : estimator object
  - **param_distributions** : dict or list of dicts
  - **n_iter** : int, default=10
  - **scoring** : str, callable, list, tuple or dict, default=None
  - **n_jobs** : int, default=None
  - **refit** : bool, str, or callable, default=True
  - **cv** : int, cross-validation generator or an iterable, default=None
  - **verbose** : int
  - **pre_dispatch** : int, or str, default=’2*n_jobs’
  - **random_state** : int, RandomState instance or None, default=None
  - **error_score** : ‘raise’ or numeric, default=np.nan
  - **return_train_score** : bool, default=False
  - **X** : array-like of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples, n_output)             or (n_samples,), default=None
  - **groups** : array-like of shape (n_samples,), default=None
  - ****fit_params** : dict of str -> object

  #### *List of attributes:*

  #### *List of attributes:*
  - **cv_results_** : dict of numpy (masked) ndarrays
  - **best_estimator_** : estimator
  - **best_score_** : float
  - **best_params_** : dict
  - **best_index_** : int
  - **scorer_** : function or a dict
  - **n_splits_** : int
  - **refit_time_** : float
  - **multimetric_** : bool
  - **feature_names_in_** : ndarray of shape (n_classes,)
  - **self** : int

  #### *List of methods:*
  - **‘rbf’** : 0.1
  - **‘rbf’** : 0.2
  - **‘rbf’** : 0.3
  - **decision_function(X)** : Call decision_function on the estimator with the best found parameters.
  - **fit(X[, y, groups])** : Run fit with all sets of parameters.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(Xt)** : Call inverse_transform on the estimator with the best found params.
  - **predict(X)** : Call predict on the estimator with the best found parameters.
  - **predict_log_proba(X)** : Call predict_log_proba on the estimator with the best found parameters.
  - **predict_proba(X)** : Call predict_proba on the estimator with the best found parameters.
  - **score(X[, y])** : Return the score on the given data, if the estimator has been refit.
  - **score_samples(X)** : Call score_samples on the estimator with the best found parameters.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Call transform on the estimator with the best found parameters.


## [*mean_squared_error*](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html)
  sklearn.metrics.mean_squared_error(y_true, y_pred, *, sample_weight=None, multioutput='uniform_average', squared=True)[source]¶

  #### *List of parameters:*
  - **y_true** : array-like of shape (n_samples,) or (n_samples, n_outputs)
  - **y_pred** : array-like of shape (n_samples,) or (n_samples, n_outputs)
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **multioutput** : {‘raw_values’, ‘uniform_average’} or array-like of shape             (n_outputs,), default=’uniform_average’
  - **squared** : bool, default=True

  #### *List of return values:*

  #### *List of attributes:*
  - **loss** : float or ndarray of floats

  #### *List of methods:*


## [*mean_absolute_error*](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_absolute_error.html)
  sklearn.metrics.mean_absolute_error(y_true, y_pred, *, sample_weight=None, multioutput='uniform_average')[source]¶

  #### *List of parameters:*
  - **y_true** : array-like of shape (n_samples,) or (n_samples, n_outputs)
  - **y_pred** : array-like of shape (n_samples,) or (n_samples, n_outputs)
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **multioutput** : {‘raw_values’, ‘uniform_average’}  or array-like of shape             (n_outputs,), default=’uniform_average’

  #### *List of return values:*

  #### *List of attributes:*
  - **loss** : float or ndarray of floats

  #### *List of methods:*


## [*mean_absolute_percentage_error*](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_absolute_percentage_error.html)
  sklearn.metrics.mean_absolute_percentage_error(y_true, y_pred, *, sample_weight=None, multioutput='uniform_average')[source]¶

  #### *List of parameters:*
  - **y_true** : array-like of shape (n_samples,) or (n_samples, n_outputs)
  - **y_pred** : array-like of shape (n_samples,) or (n_samples, n_outputs)
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **multioutput** : {‘raw_values’, ‘uniform_average’} or array-like

  #### *List of return values:*

  #### *List of attributes:*
  - **loss** : float or ndarray of floats

  #### *List of methods:*


## [*log_loss*](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.log_loss.html)
  sklearn.metrics.log_loss(y_true, y_pred, *, eps=1e-15, normalize=True, sample_weight=None, labels=None)[source]¶

  #### *List of parameters:*
  - **y_true** : array-like or label indicator matrix
  - **y_pred** : array-like of float, shape = (n_samples, n_classes) or (n_samples,)
  - **eps** : float, default=1e-15
  - **normalize** : bool, default=True
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **labels** : array-like, default=None

  #### *List of return values:*

  #### *List of attributes:*
  - **loss** : float

  #### *List of methods:*


## [*confusion_matrix*](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.confusion_matrix.html)
  sklearn.metrics.confusion_matrix(y_true, y_pred, *, labels=None, sample_weight=None, normalize=None)[source]¶

  #### *List of parameters:*
  - **y_true** : array-like of shape (n_samples,)
  - **y_pred** : array-like of shape (n_samples,)
  - **labels** : array-like of shape (n_classes), default=None
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **normalize** : {‘true’, ‘pred’, ‘all’}, default=None

  #### *List of return values:*

  #### *List of attributes:*
  - **C** : ndarray of shape (n_classes, n_classes)

  #### *List of methods:*


## [*ConfusionMatrixDisplay*](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.ConfusionMatrixDisplay.html)
  class sklearn.metrics.ConfusionMatrixDisplay(confusion_matrix, *, display_labels=None)[source]¶

  #### *List of parameters:*
  - **estimator** : estimator instance
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,)
  - **labels** : array-like of shape (n_classes,), default=None
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **normalize** : {‘true’, ‘pred’, ‘all’}, default=None
  - **display_labels** : array-like of shape (n_classes,), default=None
  - **include_values** : bool, default=True
  - **xticks_rotation** : {‘vertical’, ‘horizontal’} or float,                 default=’horizontal’
  - **values_format** : str, default=None
  - **cmap** : str or matplotlib Colormap, default=’viridis’
  - **ax** : matplotlib Axes, default=None
  - **colorbar** : bool, default=True
  - **im_kw** : dict, default=None
  - **y_true** : array-like of shape (n_samples,)
  - **y_pred** : array-like of shape (n_samples,)
  - **labels** : array-like of shape (n_classes,), default=None
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **normalize** : {‘true’, ‘pred’, ‘all’}, default=None
  - **display_labels** : array-like of shape (n_classes,), default=None
  - **include_values** : bool, default=True
  - **xticks_rotation** : {‘vertical’, ‘horizontal’} or float,                 default=’horizontal’
  - **values_format** : str, default=None
  - **cmap** : str or matplotlib Colormap, default=’viridis’
  - **ax** : matplotlib Axes, default=None
  - **colorbar** : bool, default=True
  - **im_kw** : dict, default=None
  - **include_values** : bool, default=True
  - **cmap** : str or matplotlib Colormap, default=’viridis’
  - **xticks_rotation** : {‘vertical’, ‘horizontal’} or float,                          default=’horizontal’
  - **values_format** : str, default=None
  - **ax** : matplotlib axes, default=None
  - **colorbar** : bool, default=True
  - **im_kw** : dict, default=None

  #### *List of return values:*

  #### *List of attributes:*
  - **display** : ConfusionMatrixDisplay
  - **display** : ConfusionMatrixDisplay
  - **display** : ConfusionMatrixDisplay

  #### *List of methods:*
  - **from_estimator(estimator, X, y, \*[, labels, ...])** : Plot Confusion Matrix given an estimator and some data.
  - **from_predictions(y_true, y_pred, \*[, ...])** : Plot Confusion Matrix given true and predicted labels.
  - **plot(\*[, include_values, cmap, ...])** : Plot visualization.


## [*precision_score*](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.precision_score.html)
  sklearn.metrics.precision_score(y_true, y_pred, *, labels=None, pos_label=1, average='binary', sample_weight=None, zero_division='warn')[source]¶

  #### *List of parameters:*
  - **y_true** : 1d array-like, or label indicator array / sparse matrix
  - **y_pred** : 1d array-like, or label indicator array / sparse matrix
  - **labels** : array-like, default=None
  - **pos_label** : str or int, default=1
  - **average** : {‘micro’, ‘macro’, ‘samples’, ‘weighted’, ‘binary’} or None,             default=’binary’
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **zero_division** : “warn”, 0 or 1, default=”warn”

  #### *List of return values:*

  #### *List of attributes:*
  - **precision** : float (if average is not None) or array of float of shape                 (n_unique_labels,)

  #### *List of methods:*


## [*recall_score*](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.recall_score.html)
  sklearn.metrics.recall_score(y_true, y_pred, *, labels=None, pos_label=1, average='binary', sample_weight=None, zero_division='warn')[source]¶

  #### *List of parameters:*
  - **y_true** : 1d array-like, or label indicator array / sparse matrix
  - **y_pred** : 1d array-like, or label indicator array / sparse matrix
  - **labels** : array-like, default=None
  - **pos_label** : str or int, default=1
  - **average** : {‘micro’, ‘macro’, ‘samples’, ‘weighted’, ‘binary’} or None,             default=’binary’
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **zero_division** : “warn”, 0 or 1, default=”warn”

  #### *List of return values:*

  #### *List of attributes:*
  - **recall** : float (if average is not None) or array of float of shape              (n_unique_labels,)

  #### *List of methods:*


## [*make_scorer*](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.make_scorer.html)
  sklearn.metrics.make_scorer(score_func, *, greater_is_better=True, needs_proba=False, needs_threshold=False, **kwargs)[source]¶

  #### *List of parameters:*
  - **score_func** : callable
  - **greater_is_better** : bool, default=True
  - **needs_proba** : bool, default=False
  - **needs_threshold** : bool, default=False
  - ****kwargs** : additional arguments

  #### *List of return values:*

  #### *List of attributes:*
  - **scorer** : callable

  #### *List of methods:*


## [*classification_report*](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html)
  sklearn.metrics.classification_report(y_true, y_pred, *, labels=None, target_names=None, sample_weight=None, digits=2, output_dict=False, zero_division='warn')[source]¶

  #### *List of parameters:*
  - **y_true** : 1d array-like, or label indicator array / sparse matrix
  - **y_pred** : 1d array-like, or label indicator array / sparse matrix
  - **labels** : array-like of shape (n_labels,), default=None
  - **target_names** : list of str of shape (n_labels,), default=None
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **digits** : int, default=2
  - **output_dict** : bool, default=False
  - **zero_division** : “warn”, 0 or 1, default=”warn”

  #### *List of return values:*

  #### *List of attributes:*
  - **report** : str or dict

  #### *List of methods:*


## [*roc_curve*](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.roc_curve.html)
  sklearn.metrics.roc_curve(y_true, y_score, *, pos_label=None, sample_weight=None, drop_intermediate=True)[source]¶

  #### *List of parameters:*
  - **y_true** : ndarray of shape (n_samples,)
  - **y_score** : ndarray of shape (n_samples,)
  - **pos_label** : int or str, default=None
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **drop_intermediate** : bool, default=True

  #### *List of return values:*

  #### *List of attributes:*
  - **fpr** : ndarray of shape (>2,)
  - **tpr** : ndarray of shape (>2,)
  - **thresholds** : ndarray of shape = (n_thresholds,)

  #### *List of methods:*


## [*plot_roc_curve*](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.plot_roc_curve.html)
  sklearn.metrics.plot_roc_curve(estimator, X, y, *, sample_weight=None, drop_intermediate=True, response_method='auto', name=None, ax=None, pos_label=None, **kwargs)[source]¶

  #### *List of parameters:*
  - **estimator** : estimator instance
  - **X** : {array-like, sparse matrix} of shape (n_samples, n_features)
  - **y** : array-like of shape (n_samples,)
  - **sample_weight** : array-like of shape (n_samples,), default=None
  - **drop_intermediate** : bool, default=True
  - **response_method** : {‘predict_proba’, ‘decision_function’, ‘auto’}             default=’auto’
  - **name** : str, default=None
  - **ax** : matplotlib axes, default=None
  - **pos_label** : str or int, default=None
  - ****kwargs** : dict

  #### *List of return values:*

  #### *List of attributes:*
  - **display** : RocCurveDisplay

  #### *List of methods:*


## [*PCA*](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html)
  class sklearn.decomposition.PCA(n_components=None, *, copy=True, whiten=False, svd_solver='auto', tol=0.0, iterated_power='auto', n_oversamples=10, power_iteration_normalizer='auto', random_state=None)[source]¶

  #### *List of parameters:*
  - **n_components** : int, float or ‘mle’, default=None
  - **copy** : bool, default=True
  - **whiten** : bool, default=False
  - **svd_solver** : {‘auto’, ‘full’, ‘arpack’, ‘randomized’}, default=’auto’
  - **tol** : float, default=0.0
  - **iterated_power** : int or ‘auto’, default=’auto’
  - **n_oversamples** : int, default=10
  - **power_iteration_normalizer** : {‘auto’, ‘QR’, ‘LU’, ‘none’}, default=’auto’
  - **random_state** : int, RandomState instance or None, default=None

  #### *List of attributes:*

  #### *List of attributes:*
  - **components_** : ndarray of shape (n_components, n_features)
  - **explained_variance_** : ndarray of shape (n_components,)
  - **explained_variance_ratio_** : ndarray of shape (n_components,)
  - **singular_values_** : ndarray of shape (n_components,)
  - **mean_** : ndarray of shape (n_features,)
  - **n_components_** : int
  - **n_features_** : int
  - **n_samples_** : int
  - **noise_variance_** : float
  - **n_features_in_** : int
  - **feature_names_in_** : ndarray of shape (n_features_in_,)

  #### *List of methods:*
  - **fit(X[, y])** : Fit the model with X.
  - **fit_transform(X[, y])** : Fit the model with X and apply the dimensionality reduction on X.
  - **get_covariance()** : Compute data covariance with the generative model.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **get_precision()** : Compute data precision matrix with the generative model.
  - **inverse_transform(X)** : Transform data back to its original space.
  - **score(X[, y])** : Return the average log-likelihood of all samples.
  - **score_samples(X)** : Return the log-likelihood of each sample.
  - **set_params(\*\*params)** : Set the parameters of this estimator.
  - **transform(X)** : Apply dimensionality reduction to X.


## [*Pipeline*](https://scikit-learn.org/stable/modules/generated/sklearn.pipeline.Pipeline.html)
  class sklearn.pipeline.Pipeline(steps, *, memory=None, verbose=False)[source]¶

  #### *List of parameters:*
  - **steps** : list of tuple
  - **memory** : str or object with the joblib.Memory interface, default=None
  - **verbose** : bool, default=False
  - **X** : iterable
  - ****predict_params** : dict of string -> object

  #### *List of return values:*

  #### *List of attributes:*
  - **y_pred** : Bunch

  #### *List of methods:*
  - **decision_function(X)** : Transform the data, and apply decision_function with the final estimator.
  - **fit(X[, y])** : Fit the model.
  - **fit_predict(X[, y])** : Transform the data, and apply fit_predict with the final estimator.
  - **fit_transform(X[, y])** : Fit the model and transform with the final estimator.
  - **get_feature_names_out([input_features])** : Get output feature names for transformation.
  - **get_params([deep])** : Get parameters for this estimator.
  - **inverse_transform(Xt)** : Apply inverse_transform for each step in a reverse order.
  - **predict(X, \*\*predict_params)** : Transform the data, and apply predict with the final estimator.
  - **predict_log_proba(X, \*\*predict_log_proba_params)** : Transform the data, and apply predict_log_proba with the final estimator.
  - **predict_proba(X, \*\*predict_proba_params)** : Transform the data, and apply predict_proba with the final estimator.
  - **score(X[, y, sample_weight])** : Transform the data, and apply score with the final estimator.
  - **score_samples(X)** : Transform the data, and apply score_samples with the final estimator.
  - **set_params(\*\*kwargs)** : Set the parameters of this estimator.
  - **transform(X)** : Transform the data, and apply transform with the final estimator.


## [*type_of_target*](https://scikit-learn.org/stable/modules/generated/sklearn.utils.multiclass.type_of_target.html)
  sklearn.utils.multiclass.type_of_target(y, input_name='')[source]¶

  #### *List of parameters:*
  - **y** : array-like
  - **input_name** : str, default=””

  #### *List of return values:*

  #### *List of attributes:*
  - **target_type** : str

  #### *List of methods:*