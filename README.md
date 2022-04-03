# MovieLens

1) Данные для обучения и валидации будем делить следующим образом: данные каждого пользователя отсортируем по времени, далее разобъем в соотношении 75/25, причем, если величина 25% превышает медианное значение количества просмотренных фильмов всех пользователей, то в валидационную выборку берем число данных равное медианному значению. Делаем это для того, чтобы валидация была сбалансирована.
2) В качестве метрики качества будем использовать NDCG@1 и NDCG@10, т.е. будем учитываем порядок в выборке (чем выше поставленный рейтинг, тем выше ранг).
3) По полученным данным сложно судить о том, что лучше. Потенциально LightFM с фичами для пользователей и фильмов, должен ранжировать лучше, чем ALS. Для этого было бы неплохо как минимум нормально поподбирать параметры моделей, но к сожалению вычислительные мощности не позволяют этого сделать, как и не позволили обучить lightfm-модель с использованием в фичах пользователей/фильмов информацию о тэгах.
