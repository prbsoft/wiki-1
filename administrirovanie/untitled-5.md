# Загрузка данных в документ из файла Excel или DBF

**Загрузка данных в документ из файла Excel или DBF**

Для загрузки данных в документ из файла Excel или DBF можно применить метод загрузки его в поле PBLOB таблицы TMDB\_F1M и последующего разбора по ячейкам в таблицу TMDB\_F1D. Это можно сделать вручную, включив для документа свойство "UseTabXL" и загрузив и проанализировав его при помощи кнопок на панели. Затем полученные данные в таблице TMDB\_F1D можно проанализировать на PL/SQL из Action документа и заполнить на их основании спецрегистр. Но процедуру можно упростить, если на этом Action поставить свойство "ExcelFileLoad" - тогда перед выполнением этого Action пользователю будет предложено указать файл, затем указанный файл будет загружен и разобран по ячейкам таблицы TMDB\_F1D - и процедуре на PL/SQL останется только сделать последующий анализ и обработку этих данных.

