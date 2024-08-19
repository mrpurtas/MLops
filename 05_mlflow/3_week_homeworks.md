## Soru-1
- 1.1. `lab-env` adında python 3.7 kullanan conda environment oluşturunuz.

conda create --name lab-env python=3.7
conda activate lab-env


- 1.2. Jupyter lab'ı 8991 portundan çalıştırınız.

conda install -c conda-forge jupyterlab
ipython kernel install --user --name=lab-env
jupyter lab --ip 0.0.0.0 --port 8991

---Port Forwarding---

sudo vi /Library/Preferences/VMware\ Fusion/vmnet8/nat.conf 

esc + :wq

sudo /Applications/VMware\ Fusion.app/Contents/Library/vmnet-cli --stop
sudo /Applications/VMware\ Fusion.app/Contents/Library/vmnet-cli --start



- 1.3. https://github.com/erkansirin78/datasets/raw/master/housing.csv veri seti üzerinde keşfedici veri analizi ve bazı temel görselleştirmeler yapınız. 




## Soru-2
- 2.1. Jupyter Lab notebook kullanarak https://github.com/erkansirin78/datasets/raw/master/housing.csv veri seti ile bir regresyon modeli oluşturunuz.
- 2.2. Mlflow üzerinde `HousingPricePrediction` adında bir experiment oluşturunuz.
- 2.3. Üç tane farklı model (farklı algoritma veya farklı hiper parametrelerle) Mlflow `HousingPricePrediction` altında en az iki hiperparametre ve bir tane de başarı metriği logu gönderiniz.
- 2.4. `HousingPricePrediction` deneyimlerinizi mlflow arayüzünden inceleyiniz. En başarılı modeli kaydediniz (Model registry).

