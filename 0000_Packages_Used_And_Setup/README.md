## 1. Packages Used
             import numpy as np
             import pandas as pd
             import os
             import seaborn as sns
             import matplotlib.pyplot as plt
             from sklearn.model_selection import train_test_split
             from sklearn.model_selection import KFold
             from sklearn.metrics import f1_score
             from sklearn.metrics import roc_curve
             from sklearn.metrics import auc
             from sklearn.preprocessing import StandardScaler
             from sklearn.preprocessing import LabelEncoder
             from imblearn.over_sampling import RandomOverSampler
             from imblearn.under_sampling import RandomUnderSampler
             from sklearn.metrics import average_precision_score
             from sklearn.metrics import classification_report
             from sklearn.metrics import confusion_matrix
             from sklearn.metrics import precision_recall_curve
             from tensorflow.keras.models import Sequential
             from tensorflow.keras.layers import Dense,Dropout
             from tensorflow.keras import regularizers
             from tensorflow.keras.losses import BinaryCrossentropy
             from tensorflow.keras.callbacks import EarlyStopping
             import keras_tuner as kt
             import tensorflow as tf
             from IPython import display
             import keras.backend as K
             from IPython.display import display
             from keras.wrappers.scikit_learn import KerasClassifier
             from eli5.sklearn import PermutationImportance

## 2. Random State & Random Seed
             random_state = 123
             np.random.seed(123)
