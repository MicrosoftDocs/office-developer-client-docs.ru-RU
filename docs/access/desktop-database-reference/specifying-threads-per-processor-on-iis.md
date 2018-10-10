---
title: Specifying Threads Per Processor on IIS
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de3c8c99c7f615928ea0a0f1e15171cc90b25f3d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480355"
---
# <a name="specifying-threads-per-processor-on-iis"></a>Specifying Threads Per Processor on IIS


**Применимо к**: Access 2013 | Office 2013

При использовании служб удаленных рабочих СТОЛОВ с помощью Internet Information Services 4.0 или более поздней версии, количество потоков, созданных на процессор можно управлять с помощью управления реестра на веб-сервере. Количество потоков процессора может повлиять на производительность в случае большой сетевой трафик, или в ситуациях низкой трафика с помощью запроса большого размера. Пользователю следует проверить для достижения наилучших результатов.

Метод, используемый для определения и измените значение по умолчанию для этого параметра зависит от конфигурации сервера IIS 4.0.

С MDAC 2.1.2.4202.3 (Джорджия) или более поздней версии на сервере IIS использует служб удаленных рабочих СТОЛОВ же службы компонентов (или транзакций Microsoft Services, если вы используете Windows NT) пул потоков как ASP сценариев использования. Значение по умолчанию для числа потоков на процессор — 10. Чтобы изменить значение по умолчанию, необходимо добавить следующий раздел реестра сервера:

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

где *MaxPoolThreads* — REG\_значение DWORD. *MaxPoolThreads* не отображается в реестре, если он добавляется в частности. Диапазон допустимых значений от 5 рекомендуемый максимум 20. Если значение, указанное в ключе реестра больше, чем значение параметра *PoolThreadLimit* (находится в разделе тот же путь), используется значение *PoolThreadLimit* .

Кроме того Если MDAC 2.1 2.1.1.3711.11 (Джорджия) или более ранних версий установлен на сервере служб IIS, значение по умолчанию для числа потоков процессора, 6. Чтобы изменить значение по умолчанию, необходимо добавить следующий раздел реестра на сервере IIS:

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

где *ADCThreads* — REG\_значение DWORD. *ADCThreads* не отображается в реестре, если он добавляется в частности. Диапазон допустимые значения — от 1 до 50. Если значение, указанное в ключе реестра больше 50, максимальное значение — используемых (50).
