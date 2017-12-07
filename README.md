# Face-Detection

1) Unzip the images directory
2) Download the model: http://download.tensorflow.org/models/object_detection/ssd_mobilenet_v1_coco_11_06_2017.tar.gz
3) Run train.py using: 'python3 train.py --logtostderr --train_dir=training --pipeline_config_path=training/ssd_mobilenet_v1_pets.config'

After Training:-
python3 export_inference_graph.py \
    --input_type image_tensor \
    --pipeline_config_path training/ssd_mobilenet_v1_pets.config \
    --trained_checkpoint_prefix training/model.ckpt-<number> \
    --output_directory face_det_graph
  <number> is the step number of the last checkpoint. Check training directory for the last checkpoint number.
    
Run jupyter notebook    
