# GRT INSTALLATION




##### References

https://github.com/nickgillian/grt

http://nickgillian.com/grt/api/0.1.0/index.html

http://www.nickgillian.com/wiki/pmwiki.php/GRT/GestureRecognitionToolkit


# INSTALLATION on Ubuntu

```
$ uname -a
Linux eee320 3.13.0-92-generic #139-Ubuntu
SMP Tue Jun 28 20:42:26 UTC 2016 x86_64 x86_64 x86_64 GNU/Linux
```

```
$ lsb_release -a
No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 14.04.3 LTS
Release:	14.04
Codename:	trusty
```

### terminal Output

You can build the GRT as a shared library and compile the examples examples by:
open terminal and cd to this build directory create a temporary build folder:

```
$ mkdir tmp
```
cd to the temporary build folder:

```
$ cd tmp
```
use cmake to generate the makefile for your machine:
```
$ cmake ..
```
compile the GRT library and examples (j controls the number of cores you want to use, N == the number of cores):
```
$ make -jN
```
you can then install the GRT by running:
```
$ sudo make install
```


```
$ sudo make install
[sudo] password for map479-admin:
[ 60%] Built target grt
[ 60%] Built target ANBCExample
[ 61%] Built target AdaBoostExample
[ 61%] Built target BAGExample
[ 62%] Built target CircularBufferExample
[ 62%] Built target ClassLabelChangeFilterExample
[ 63%] Built target ClassLabelFilterExample
[ 63%] Built target ClassLabelTimeoutFilterExample
[ 64%] Built target ClassificationDataExample
[ 65%] Built target ClusterTreeExample
[ 65%] Built target CommandLineParser
[ 67%] Built target CustomFeatureExtraction
[ 67%] Built target CustomMakefile
[ 68%] Built target DTWExample
[ 68%] Built target DeadZoneExample
[ 69%] Built target DecisionTreeExample
[ 70%] Built target DerivativeExample
[ 70%] Built target DoubleMovingAverageFilterExample
[ 71%] Built target FFTExample
[ 71%] Built target FFTFeaturesExample
[ 72%] Built target GMMExample
[ 72%] Built target GaussianMixtureModelsExample
[ 73%] Built target GettingStarted
[ 73%] Built target GridSearchExample
[ 74%] Built target HMMContinuousExample
[ 75%] Built target HMMDiscreteExample
[ 75%] Built target HelloWorldExample
[ 76%] Built target HighPassFilterExample
[ 76%] Built target KMeansExample
[ 77%] Built target KMeansQuantizerExample
[ 77%] Built target KNNExample
[ 78%] Built target LeakyIntegratorExample
[ 78%] Built target LinearRegressionExample
[ 79%] Built target LogisticRegressionExample
[ 80%] Built target LowPassFilterExample
[ 80%] Built target MLPRegressionExample
[ 81%] Built target MachineLearning101
[ 81%] Built target MatrixExample
[ 82%] Built target MatrixFloatExample
[ 83%] Built target gtest
[ 83%] Built target MatrixTest
[ 84%] Built target MedianFilterExample
[ 84%] Built target MinDistExample
[ 85%] Built target MovementIndexExample
[ 86%] Built target MovingAverageFilterExample
[ 86%] Built target MultidimensionalRegressionExample
[ 87%] Built target PrincipalComponentAnalysisExample
[ 87%] Built target RandomExample
[ 88%] Built target RandomForestsExample
[ 88%] Built target RegressionDataExample
[ 89%] Built target SVDExample
[ 89%] Built target SVMExample
[ 90%] Built target SavitskyGolayFilterExample
[ 91%] Built target SoftmaxExample
[ 91%] Built target ThreadPoolExample
[ 92%] Built target TimeSeriesClassificationDataExample
[ 92%] Built target TimeSeriesClassificationDataStreamExample
[ 93%] Built target TypedefsTest
[ 93%] Built target UnlabelledDataExample
[ 94%] Built target UtilExample
[ 94%] Built target VectorFloatTest
[ 95%] Built target VectorTest
[ 96%] Built target ZeroCrossingCounterExample
[ 97%] Built target grt-lin-reg-tool
[ 97%] Built target grt-log-reg-tool
[ 98%] Built target grt-merge-tool
[ 98%] Built target grt-rf-tool
[100%] Built target grt-split-tool
[100%] Built target grt-test-tool
Install the project...
-- Install configuration: ""
-- Installing: /usr/local/lib/libgrt.so
-- Installing: /usr/local/include/GRT
-- Installing: /usr/local/include/GRT/Util
-- Installing: /usr/local/include/GRT/Util/TrainingResult.h
-- Installing: /usr/local/include/GRT/Util/DataType.h
-- Installing: /usr/local/include/GRT/Util/ClassificationResult.h
-- Installing: /usr/local/include/GRT/Util/Cholesky.h
-- Installing: /usr/local/include/GRT/Util/TestInstanceResult.h
-- Installing: /usr/local/include/GRT/Util/TimeSeriesClassificationSampleTrimmer.h
-- Installing: /usr/local/include/GRT/Util/FileParser.h
-- Installing: /usr/local/include/GRT/Util/ThresholdCrossingDetector.h
-- Installing: /usr/local/include/GRT/Util/TestResult.h
-- Installing: /usr/local/include/GRT/Util/RangeTracker.h
-- Installing: /usr/local/include/GRT/Util/Random.h
-- Installing: /usr/local/include/GRT/Util/GRTVersionInfo.h
-- Installing: /usr/local/include/GRT/Util/DebugLog.h
-- Installing: /usr/local/include/GRT/Util/MinMax.h
-- Installing: /usr/local/include/GRT/Util/CircularBuffer.h
-- Installing: /usr/local/include/GRT/Util/ThreadPool.h
-- Installing: /usr/local/include/GRT/Util/GRTCommon.h
-- Installing: /usr/local/include/GRT/Util/CommandLineParser.h
-- Installing: /usr/local/include/GRT/Util/GRTTypedefs.h
-- Installing: /usr/local/include/GRT/Util/IndexedDouble.h
-- Installing: /usr/local/include/GRT/Util/InfoLog.h
-- Installing: /usr/local/include/GRT/Util/LUDecomposition.h
-- Installing: /usr/local/include/GRT/Util/SVD.h
-- Installing: /usr/local/include/GRT/Util/TrainingDataRecordingTimer.h
-- Installing: /usr/local/include/GRT/Util/Timer.h
-- Installing: /usr/local/include/GRT/Util/TrainingLog.h
-- Installing: /usr/local/include/GRT/Util/ObserverManager.h
-- Installing: /usr/local/include/GRT/Util/ErrorLog.h
-- Installing: /usr/local/include/GRT/Util/TimeStamp.h
-- Installing: /usr/local/include/GRT/Util/Util.h
-- Installing: /usr/local/include/GRT/Util/EigenvalueDecomposition.h
-- Installing: /usr/local/include/GRT/Util/Log.h
-- Installing: /usr/local/include/GRT/Util/GRTException.h
-- Installing: /usr/local/include/GRT/Util/TestingLog.h
-- Installing: /usr/local/include/GRT/Util/WarningLog.h
-- Installing: /usr/local/include/GRT/Util/Observer.h
-- Installing: /usr/local/include/GRT/Util/ClassTracker.h
-- Installing: /usr/local/include/GRT/Util/PeakDetection.h
-- Installing: /usr/local/include/GRT/PreProcessingModules
-- Installing: /usr/local/include/GRT/PreProcessingModules/MedianFilter.h
-- Installing: /usr/local/include/GRT/PreProcessingModules/DeadZone.h
-- Installing: /usr/local/include/GRT/PreProcessingModules/FIRFilter.h
-- Installing: /usr/local/include/GRT/PreProcessingModules/SavitzkyGolayFilter.h
-- Installing: /usr/local/include/GRT/PreProcessingModules/LeakyIntegrator.h
-- Installing: /usr/local/include/GRT/PreProcessingModules/HighPassFilter.h
-- Installing: /usr/local/include/GRT/PreProcessingModules/LowPassFilter.h
-- Installing: /usr/local/include/GRT/PreProcessingModules/MovingAverageFilter.h
-- Installing: /usr/local/include/GRT/PreProcessingModules/DoubleMovingAverageFilter.h
-- Installing: /usr/local/include/GRT/PreProcessingModules/WeightedAverageFilter.h
-- Installing: /usr/local/include/GRT/PreProcessingModules/Derivative.h
-- Installing: /usr/local/include/GRT/PostProcessingModules
-- Installing: /usr/local/include/GRT/PostProcessingModules/ClassLabelFilter.h
-- Installing: /usr/local/include/GRT/PostProcessingModules/ClassLabelTimeoutFilter.h
-- Installing: /usr/local/include/GRT/PostProcessingModules/ClassLabelChangeFilter.h
-- Installing: /usr/local/include/GRT/ContextModules
-- Installing: /usr/local/include/GRT/ContextModules/Gate.h
-- Installing: /usr/local/include/GRT/ClusteringModules
-- Installing: /usr/local/include/GRT/ClusteringModules/KMeans
-- Installing: /usr/local/include/GRT/ClusteringModules/KMeans/KMeans.h
-- Installing: /usr/local/include/GRT/ClusteringModules/ClusterTree
-- Installing: /usr/local/include/GRT/ClusteringModules/ClusterTree/ClusterTreeNode.h
-- Installing: /usr/local/include/GRT/ClusteringModules/ClusterTree/ClusterTree.h
-- Installing: /usr/local/include/GRT/ClusteringModules/HierarchicalClustering
-- Installing: /usr/local/include/GRT/ClusteringModules/HierarchicalClustering/HierarchicalClustering.h
-- Installing: /usr/local/include/GRT/ClusteringModules/GaussianMixtureModels
-- Installing: /usr/local/include/GRT/ClusteringModules/GaussianMixtureModels/GaussianMixtureModels.h
-- Installing: /usr/local/include/GRT/ClusteringModules/SelfOrganizingMap
-- Installing: /usr/local/include/GRT/ClusteringModules/SelfOrganizingMap/SelfOrganizingMap.h
-- Installing: /usr/local/include/GRT/RegressionModules
-- Installing: /usr/local/include/GRT/RegressionModules/LogisticRegression
-- Installing: /usr/local/include/GRT/RegressionModules/LogisticRegression/LogisticRegression.h
-- Installing: /usr/local/include/GRT/RegressionModules/LinearRegression
-- Installing: /usr/local/include/GRT/RegressionModules/LinearRegression/LinearRegression.h
-- Installing: /usr/local/include/GRT/RegressionModules/MultidimensionalRegression
-- Installing: /usr/local/include/GRT/RegressionModules/MultidimensionalRegression/MultidimensionalRegression.h
-- Installing: /usr/local/include/GRT/RegressionModules/RegressionTree
-- Installing: /usr/local/include/GRT/RegressionModules/RegressionTree/RegressionTree.h
-- Installing: /usr/local/include/GRT/RegressionModules/RegressionTree/RegressionTreeNode.h
-- Installing: /usr/local/include/GRT/RegressionModules/ArtificialNeuralNetworks
-- Installing: /usr/local/include/GRT/RegressionModules/ArtificialNeuralNetworks/MLP
-- Installing: /usr/local/include/GRT/RegressionModules/ArtificialNeuralNetworks/MLP/MLP.h
-- Installing: /usr/local/include/GRT/RegressionModules/ArtificialNeuralNetworks/MLP/Neuron.h
-- Installing: /usr/local/include/GRT/DataStructures
-- Installing: /usr/local/include/GRT/DataStructures/Vector.h
-- Installing: /usr/local/include/GRT/DataStructures/RegressionData.h
-- Installing: /usr/local/include/GRT/DataStructures/Matrix.h
-- Installing: /usr/local/include/GRT/DataStructures/VectorFloat.h
-- Installing: /usr/local/include/GRT/DataStructures/ClassificationDataStream.h
-- Installing: /usr/local/include/GRT/DataStructures/MatrixFloat.h
-- Installing: /usr/local/include/GRT/DataStructures/TimeSeriesPositionTracker.h
-- Installing: /usr/local/include/GRT/DataStructures/UnlabelledData.h
-- Installing: /usr/local/include/GRT/DataStructures/TimeSeriesClassificationData.h
-- Installing: /usr/local/include/GRT/DataStructures/RegressionSample.h
-- Installing: /usr/local/include/GRT/DataStructures/TimeSeriesClassificationSample.h
-- Installing: /usr/local/include/GRT/DataStructures/ClassificationData.h
-- Installing: /usr/local/include/GRT/DataStructures/ClassificationSample.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms
-- Installing: /usr/local/include/GRT/CoreAlgorithms/MeanShift
-- Installing: /usr/local/include/GRT/CoreAlgorithms/MeanShift/MeanShift.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/LeastSquares
-- Installing: /usr/local/include/GRT/CoreAlgorithms/LeastSquares/LinearLeastSquares.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/MovementDetector
-- Installing: /usr/local/include/GRT/CoreAlgorithms/MovementDetector/MovementDetector.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/ParticleFilter
-- Installing: /usr/local/include/GRT/CoreAlgorithms/ParticleFilter/ParticleFilter.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/ParticleFilter/Particle.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/PrincipalComponentAnalysis
-- Installing: /usr/local/include/GRT/CoreAlgorithms/PrincipalComponentAnalysis/PrincipalComponentAnalysis.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/EvolutionaryAlgorithm
-- Installing: /usr/local/include/GRT/CoreAlgorithms/EvolutionaryAlgorithm/EvolutionaryAlgorithm.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/EvolutionaryAlgorithm/Individual.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/Tree
-- Installing: /usr/local/include/GRT/CoreAlgorithms/Tree/Node.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/Tree/Tree.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/ParticleSwarmOptimization
-- Installing: /usr/local/include/GRT/CoreAlgorithms/ParticleSwarmOptimization/ParticleSwarmOptimization.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/ParticleSwarmOptimization/PSOParticle.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/GridSearch
-- Installing: /usr/local/include/GRT/CoreAlgorithms/GridSearch/GridSearch.h
-- Installing: /usr/local/include/GRT/CoreAlgorithms/BernoulliRBM
-- Installing: /usr/local/include/GRT/CoreAlgorithms/BernoulliRBM/BernoulliRBM.h
-- Installing: /usr/local/include/GRT/CoreModules
-- Installing: /usr/local/include/GRT/CoreModules/Classifier.h
-- Installing: /usr/local/include/GRT/CoreModules/GRTBase.h
-- Installing: /usr/local/include/GRT/CoreModules/Regressifier.h
-- Installing: /usr/local/include/GRT/CoreModules/PostProcessing.h
-- Installing: /usr/local/include/GRT/CoreModules/FeatureExtraction.h
-- Installing: /usr/local/include/GRT/CoreModules/MLBase.h
-- Installing: /usr/local/include/GRT/CoreModules/Context.h
-- Installing: /usr/local/include/GRT/CoreModules/Clusterer.h
-- Installing: /usr/local/include/GRT/CoreModules/GestureRecognitionPipeline.h
-- Installing: /usr/local/include/GRT/CoreModules/PreProcessing.h
-- Installing: /usr/local/include/GRT/GRT.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/RBMQuantizer
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/RBMQuantizer/RBMQuantizer.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/FFT
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/FFT/FastFourierTransform.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/FFT/FFTFeatures.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/FFT/FFT.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/KMeansFeatures
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/KMeansFeatures/KMeansFeatures.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/MovementTrajectoryFeatures
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/MovementTrajectoryFeatures/MovementTrajectoryFeatures.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/MovementIndex
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/MovementIndex/MovementIndex.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/SOMQuantizer
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/SOMQuantizer/SOMQuantizer.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/KMeansQuantizer
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/KMeansQuantizer/KMeansQuantizer.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/EnvelopeExtractor
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/EnvelopeExtractor/EnvelopeExtractor.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/TimeseriesBuffer
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/TimeseriesBuffer/TimeseriesBuffer.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/ZeroCrossingCounter
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/ZeroCrossingCounter/ZeroCrossingCounter.h
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/TimeDomainFeatures
-- Installing: /usr/local/include/GRT/FeatureExtractionModules/TimeDomainFeatures/TimeDomainFeatures.h
-- Installing: /usr/local/include/GRT/ClassificationModules
-- Installing: /usr/local/include/GRT/ClassificationModules/MinDist
-- Installing: /usr/local/include/GRT/ClassificationModules/MinDist/MinDist.h
-- Installing: /usr/local/include/GRT/ClassificationModules/MinDist/MinDistModel.h
-- Installing: /usr/local/include/GRT/ClassificationModules/SwipeDetector
-- Installing: /usr/local/include/GRT/ClassificationModules/SwipeDetector/SwipeDetector.h
-- Installing: /usr/local/include/GRT/ClassificationModules/HMM
-- Installing: /usr/local/include/GRT/ClassificationModules/HMM/HMM.h
-- Installing: /usr/local/include/GRT/ClassificationModules/HMM/HMMEnums.h
-- Installing: /usr/local/include/GRT/ClassificationModules/HMM/DiscreteHiddenMarkovModel.h
-- Installing: /usr/local/include/GRT/ClassificationModules/HMM/ContinuousHiddenMarkovModel.h
-- Installing: /usr/local/include/GRT/ClassificationModules/ANBC
-- Installing: /usr/local/include/GRT/ClassificationModules/ANBC/ANBC_Model.h
-- Installing: /usr/local/include/GRT/ClassificationModules/ANBC/ANBC.h
-- Installing: /usr/local/include/GRT/ClassificationModules/RandomForests
-- Installing: /usr/local/include/GRT/ClassificationModules/RandomForests/RandomForests.h
-- Installing: /usr/local/include/GRT/ClassificationModules/LDA
-- Installing: /usr/local/include/GRT/ClassificationModules/LDA/LDA.h
-- Installing: /usr/local/include/GRT/ClassificationModules/GMM
-- Installing: /usr/local/include/GRT/ClassificationModules/GMM/GMM.h
-- Installing: /usr/local/include/GRT/ClassificationModules/GMM/MixtureModel.h
-- Installing: /usr/local/include/GRT/ClassificationModules/FiniteStateMachine
-- Installing: /usr/local/include/GRT/ClassificationModules/FiniteStateMachine/FSMParticle.h
-- Installing: /usr/local/include/GRT/ClassificationModules/FiniteStateMachine/FSMParticleFilter.h
-- Installing: /usr/local/include/GRT/ClassificationModules/FiniteStateMachine/FiniteStateMachine.h
-- Installing: /usr/local/include/GRT/ClassificationModules/BAG
-- Installing: /usr/local/include/GRT/ClassificationModules/BAG/BAG.h
-- Installing: /usr/local/include/GRT/ClassificationModules/DecisionTree
-- Installing: /usr/local/include/GRT/ClassificationModules/DecisionTree/DecisionTreeClusterNode.h
-- Installing: /usr/local/include/GRT/ClassificationModules/DecisionTree/DecisionTreeTripleFeatureNode.h
-- Installing: /usr/local/include/GRT/ClassificationModules/DecisionTree/DecisionTreeThresholdNode.h
-- Installing: /usr/local/include/GRT/ClassificationModules/DecisionTree/DecisionTreeNode.h
-- Installing: /usr/local/include/GRT/ClassificationModules/DecisionTree/DecisionTree.h
-- Installing: /usr/local/include/GRT/ClassificationModules/DTW
-- Installing: /usr/local/include/GRT/ClassificationModules/DTW/DTW.h
-- Installing: /usr/local/include/GRT/ClassificationModules/KNN
-- Installing: /usr/local/include/GRT/ClassificationModules/KNN/KNN.h
-- Installing: /usr/local/include/GRT/ClassificationModules/ParticleClassifier
-- Installing: /usr/local/include/GRT/ClassificationModules/ParticleClassifier/ParticleClassifier.h
-- Installing: /usr/local/include/GRT/ClassificationModules/ParticleClassifier/ParticleClassifierParticleFilter.h
-- Installing: /usr/local/include/GRT/ClassificationModules/AdaBoost
-- Installing: /usr/local/include/GRT/ClassificationModules/AdaBoost/AdaBoostClassModel.h
-- Installing: /usr/local/include/GRT/ClassificationModules/AdaBoost/WeakClassifiers
-- Installing: /usr/local/include/GRT/ClassificationModules/AdaBoost/WeakClassifiers/WeakClassifier.h
-- Installing: /usr/local/include/GRT/ClassificationModules/AdaBoost/WeakClassifiers/DecisionStump.h
-- Installing: /usr/local/include/GRT/ClassificationModules/AdaBoost/WeakClassifiers/RadialBasisFunction.h
-- Installing: /usr/local/include/GRT/ClassificationModules/AdaBoost/AdaBoost.h
-- Installing: /usr/local/include/GRT/ClassificationModules/Softmax
-- Installing: /usr/local/include/GRT/ClassificationModules/Softmax/Softmax.h
-- Installing: /usr/local/include/GRT/ClassificationModules/Softmax/SoftmaxModel.h
-- Installing: /usr/local/include/GRT/ClassificationModules/SVM
-- Installing: /usr/local/include/GRT/ClassificationModules/SVM/LIBSVM
-- Installing: /usr/local/include/GRT/ClassificationModules/SVM/LIBSVM/libsvm.h
-- Installing: /usr/local/include/GRT/ClassificationModules/SVM/SVM.h
-- Installing: /usr/local/bin/grt-split-tool
-- Removed runtime path from "/usr/local/bin/grt-split-tool"
-- Installing: /usr/local/bin/grt-rf-tool
-- Removed runtime path from "/usr/local/bin/grt-rf-tool"
-- Installing: /usr/local/bin/grt-test-tool
-- Removed runtime path from "/usr/local/bin/grt-test-tool"
-- Installing: /usr/local/bin/grt-log-reg-tool
-- Removed runtime path from "/usr/local/bin/grt-log-reg-tool"
-- Installing: /usr/local/bin/grt-lin-reg-tool
-- Removed runtime path from "/usr/local/bin/grt-lin-reg-tool"
-- Installing: /usr/local/bin/grt-merge-tool
-- Removed runtime path from "/usr/local/bin/grt-merge-tool"
-- Installing: /usr/local/lib/x86_64-linux-gnu/pkgconfig/grt.pc
```
