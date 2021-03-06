# Определение стоимости автомобиля

**Описание проекта:** необходимо построить модель для определения стоимости автомобиля по историческим данным (технические характеристики, комплектации и цены автомобилей).

**Описание данных**
- Признаки: DateCrawled (дата скачивания анкеты из базы), VehicleType (тип автомобильного кузова), RegistrationYear (год регистрации автомобиля), Gearbox (тип коробки передач), Power (мощность в л. с.), Model (модель автомобиля), Kilometer (пробег в км), RegistrationMonth (месяц регистрации автомобиля), FuelType (тип топлива), Brand (марка автомобиля), NotRepaired (была машина в ремонте или нет), DateCreated (дата создания анкеты), NumberOfPictures (количество фотографий автомобиля), PostalCode (почтовый индекс владельца анкеты), LastSeen (дата последней активности пользователя).
- Целевой признак: Price (цена в евро).

**Технические детали реализации:**
- данные изучены и предобработанны (найдены и описаны ошибочные/невозможные значения, обработаны пропуски);
- для сравнения обучено три модели (LinearRegression, LightGBM, RandomForestRegressor);
- подбор гиперпараметров и кросс-валидация осуществлены средствами RandomizedSearchCV;
- использована кастомная метрика качества;
- на основании сводной таблицы по результатам всех моделей, RMSE на валидационной выборке и время обучения, выбрана лучшая модель;
- путем сравнения RMSE валидационной выборки с тем же показателем константной модели проверена адекватность модели.

**Используемые библиотеки:** pandas, numpy, seaborn, matplotlib, sklearn, lightgbm.
