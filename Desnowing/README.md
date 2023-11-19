### Download the Datasets
- SRRS [[gdrive](https://drive.google.com/file/d/11h1cZ0NXx6ev35cl5NKOAL3PCgLlWUl2/view?usp=sharing), [Baidu](https://pan.baidu.com/s/1VXqsamkl12fPsI1Qek97TQ?pwd=vcfg)]
- CSD [[gdrive](https://drive.google.com/file/d/1pns-7uWy-0SamxjA40qOCkkhSu7o7ULb/view?usp=sharing), [Baidu](https://pan.baidu.com/s/1N52Jnx0co9udJeYrbd3blA?pwd=sb4a)]
- Snow100K [[gdrive](https://drive.google.com/file/d/19zJs0cJ6F3G3IlDHLU2BO7nHnCTMNrIS/view?usp=sharing), [Baidu](https://pan.baidu.com/s/1QGd5z9uM6vBKPnD5d7jQmA?pwd=aph4)]

### Training

~~~
python main.py --mode train --data_dir your_path/CSD
~~~

### Evaluation
#### Download the model [here](https://drive.google.com/drive/folders/1bZb9L660t4jL2wAqr23iTg6eyAnCuUBt?usp=sharing)
#### Testing
~~~
python main.py --data_dir your_path/CSD
~~~

For training and testing, your directory structure should look like this

`Your path` <br/>
 `├──CSD` <br/>
     `├──train2500`  <br/>
          `├──Gt`  <br/>
          `└──Snow`  
     `└──test2000`  <br/>
          `├──Gt`  <br/>
          `└──Snow`  
 `├──SRRS` <br/>
     `├──train2500`  <br/>
          `├──Gt`  <br/>
          `└──Snow`  
     `└──test2000`  <br/>
          `├──Gt`  <br/>
          `└──Snow`  
 `└──Snow100K` <br/>
     `├──train2500`  <br/>
          `├──Gt`  <br/>
          `└──Snow`  
     `└──test2000`  <br/>
          `├──Gt`  <br/>
          `└──Snow`  
