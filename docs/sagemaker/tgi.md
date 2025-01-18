# Text Generation Inference (TGI) Images

[TGI](https://huggingface.co/docs/text-generation-inference/en/index) is a toolkit for deploying and serving Large Language Models (LLMs). TGI enables high-performance text generation for the most popular open-source LLMs, including Llama, Falcon, StarCoder, BLOOM, GPT-NeoX, and T5.

Below, you can find a list of the latest available images for TGI for use on AWS SageMaker.

<!-- START AUTOGEN TABLE -->
## huggingface-pytorch-tgi-inference

| Framework Version | Image Type | Image URI | Size (GB) | Pushed At | Details |
| --- | --- | --- | --- | --- | --- |
| 2.4 | gpu | `763104351884.dkr.ecr.us-west-2.amazonaws.com/huggingface-pytorch-tgi-inference:2.4.0-tgi3.0.1-gpu-py311-cu124-ubuntu22.04-v2.0` | 6.49 | 2025-01-09 21:02:36 | [Details](https://github.com/aws/deep-learning-containers/blob/master/available_images.md#huggingface-text-generation-inference-tgi-containers) |
| 2.3 | gpu | `763104351884.dkr.ecr.us-west-2.amazonaws.com/huggingface-pytorch-tgi-inference:2.3.0-tgi2.2.0-gpu-py310-cu121-ubuntu22.04-v2.1` | 4.92 | 2024-10-04 21:59:12 | [Details](https://github.com/aws/deep-learning-containers/blob/master/available_images.md#huggingface-text-generation-inference-tgi-containers) |


### SM Example
```
# create Hugging Face Model Class
huggingface_model = HuggingFaceModel(
	image_uri=get_huggingface_llm_image_uri("huggingface",version="2.4"),
	env=<insert_hub_obj>,
	role=<insert_role>, 
)

# deploy model to SageMaker Inference
predictor = huggingface_model.deploy(
	initial_instance_count=1,
	instance_type="ml.g6.48xlarge",
	container_startup_health_check_timeout=2400,
)
```
                          
<!-- END AUTOGEN TABLE -->