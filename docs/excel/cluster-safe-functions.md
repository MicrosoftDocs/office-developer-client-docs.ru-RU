---
title: Безопасные для кластера функции
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f73f49e4d76a8545399eede283b70551ee6569f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807137"
---
# <a name="cluster-safe-functions"></a>Безопасные для кластера функции

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
В Excel 2013 Excel может снизить нагрузку звонки пользовательские функции (UDF) в кластере высокопроизводительных сетей через интерфейс соединителя выделенного кластера. Поставщики COMPUTE cluster предоставляют соединителей кластеров. Авторы UDF можно объявить их пользовательских функций как кластера надежных и, при наличии соединитель кластера Excel отправляет звонков на этих пользовательских функций в соединитель кластера для разгрузки.
  
Когда Excel обнаруживает UDF кластера safe во время пересчета, передает имя XLL, на котором в настоящее время работает, имя кластера safe UDF и каких-либо параметров в соединитель кластера. Соединитель удаленно выполняется вызов пользовательских Функций и возвращает результаты в Excel. Независимые Расчет продолжается и после завершения выполнения пользовательской функции соединителя кластера передает результаты в Excel, и зависимые вычисления продолжить. Механизм это асинхронных напоминающего механизм, используемый асинхронных пользовательских функций, за исключением того, что соединитель кластера управляет асинхронные аспекты вместо автора пользовательских Функций. Как правило соединитель кластера реализует XLL оболочки совместимости для загрузки XLL-модулей и запуск пользовательских функций на вычислительном узлах кластера.
  
Механизм объявление пользовательских функций как безопасный кластера похожи объявления пользовательских функций как безопасные для многопотоковых пересчета. Тем не менее поскольку UDF не работает на том же компьютере, что и других пользовательских функций из одного сеанса Excel обязательно, существуют разные аспекты при записи безопасного кластера пользовательских функций.
  
Для регистрации пользовательской функции в качестве безопасных кластера, необходимо вызвать функцию обратного вызова [xlfRegister (формы 1)](xlfregister-form-1.md) через интерфейс **Excel12** или **Excel12v** . Дополнительные сведения об этих интерфейсах можно [Excel4/Excel12](excel4-excel12.md) и [Excel4v/Excel12v](excel4v-excel12v.md). Регистрация UDF как безопасный кластера с использованием **Excel4** или **Excel4v** интерфейса не поддерживается. 
  
Если зарегистрировать функцию в качестве безопасных кластера следует убедиться, что функция ведет себя в кластере безопасным способом. Несмотря на то, что точное поведение соединитель кластера зависит от реализации, следует разработать вашей UDF для запуска в распределенной компьютерной системе и обладают следующими характеристиками:
  
- Пользовательской функции не следует полагаться на любой оперативной памяти. Например, для пользовательской функции не следует полагаться на существующий кэш памяти.
    
- Пользовательской функции не следует выполнять обратные вызовы Excel, которые не поддерживают поставщика соединитель кластера.
    
В дополнение к поведение кластера safe существует следующие технические ограничения на кластер safe пользовательских функций.
  
1. Аргументы XLOPER (типов «P», «R»).
    
2. Аргументы XLOPER12, которые поддерживают диапазон ссылки (тип «U»).
    
3. Не может быть эквивалентную функцию листа макросов («#» и "&amp;" нельзя сочетать).
    
Для пользовательских функций с меньшие времени выполнения затрат на разгрузки может быть больше, чем время, затраченное UDF для выполнения, операция над значением преимущества использования этой инфраструктуры.
  
> [!NOTE]
> Невозможно объявить UDF safe кластер как асинхронных пользовательских Функций. 
  
Пользовательской функции можно определить, является ли он выполняется с помощью соединитель кластера с помощью вызова функции обратного вызова [xlRunningOnCluster](xlrunningoncluster.md) . 
  
