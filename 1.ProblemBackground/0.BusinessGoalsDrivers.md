# Business Goals, Drivers

# Background

[Wildlife.ai](http://Wildlife.ai) is a charitable trust that uses artificial intelligence to accelerate wildlife conservation. As such, the organization promotes community events, seminars and educational activities, all with the aim of protect biodiversity by leveraging machine learning technology.

They focus on grassroots wildlife conservation projects. Therefore, the following aspects need to be considered. From the research institution perspective, the quality of collected scientific evidence is of the highest precedence. From the non-profit perspective, the operational costs need to be reduced to a minimum in order to sustain the activities.

# Business goals

The proposed architecture starts with the organization’s mission statement: “Using artificial intelligence to accelerate wildlife conservation.” To achieve that conservation practitioners need accurate and real time information. One way of doing so is to deploy solutions that would help in automating repetitive tasks. Species identification and unique animal counting are two challenges in pressing needs of a solution, as they are the building blocks for testing more complex scientific hypothesis.

Currently, the Wildlife Watcher camera is deployed for Wētā insects detection. The final solution aims for a modular design adapted to monitor varying species. The proposed architecture should aim to serve those goals in order to enable real-time ecosystem health. All that should be done through an open-source community while educating and empowering citizen scientists of all ages to contribute to the conservation causes.

That is currently achieved through a camera which aims to address the monitoring automation requirements. That camera needs to run a machine learning model on the edge, to ease the burden on the biologists. To achieve full automation, a iterative process of machine learning model building and evaluation is required. That process includes the collection of model input samples, their annotation for target output labels, model training on the built dataset and storage of the build model as a deployment unit. With such a repository of trained models, the community could decide which models belong to which areas. The models are then sent to the corresponding cameras and configured for evaluation of the model performance. With enough confidence in built models, the solutions can be run with certainty to perform the automation tasks with satisfying level of confidence.

# Business drivers

1. Prove that the automated solutions can provide quality wildlife measurements, exceeding competing alternatives, at a lower price point.
2. Ability to successfully monitor an area will enable scientists to control for experiment variables.
3. Grow the community of biologists, nature enthusiasts, data scientists and open source makers while developing a product that fits their needs.
4. To ensure artificial intelligence is widely applied to protect biodiversity and accelerating efficient species conservation.
