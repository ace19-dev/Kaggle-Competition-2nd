### Model features
| Network Name    | Architecture                                                          | Filter Size (w, h, ?, c)                                                                      | Feature Size (w, h, c)                                                                            | Memory Usage |
|-----------------|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|--------------|
| M1              | Conv1 </br> relu </br> max pool </br> fire1 </br> fire2 </br> fire3 </br> max pool </br> fire4 </br> fire5 </br> dropout </br> Conv2 </br> relu </br> avg pool                     | Conv1 2 x 2 x 1 x 64  </br> Conv2 1 x 1 x 256 x 1000                                 | 65 x 40 x 1 </br> 33 x 20 x 64 </br> 16 x 10 x 64 </br> 16 x 10 x 128 </br> 8 x 5 x 128 </br> 8 x 5 x 256 </br> 4 x 3 x 1000 </br> 2 x 1 x 1000                                       | 175K        |
</br>
</br>

### Results
| Model           | Accuracy                                                             | Traning Step                                                                 | Learning Rate                                                                      | batch_size                        | optimizer                | activation function | silence_percentage | unknown_percentage | time_shift_ms | sample_rate |
|-----------------|------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-----------------------------------|--------------------------|---------------------|--------------------|--------------------|---------------|-------------|
| M1              | 89.2%                                                            | 15000                                                                   | 0.001                                                                  | 100                               | GradientDescentOptimizer | Relu                | 10                 | 10                 | 100           | 16000       |
|                 |                                                                  |                                                                              |                                                                                    |                                   |                          |                     |                    |                    |               |             |
</br>
</br>

### Tensorboard
![alt text](https://i.imgur.com/GmguEqN.jpg)