---
title: Метод stat - ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3853c42fab9de9e06691ae0e8efe20e23c410121
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949294"
---
# <a name="stat-method-ado"></a>Метод Stat (ADO)

**Применимо к**: Access 2013, Office 2013

Извлекает сведения о объект **Stream** .

## <a name="syntax"></a>Синтаксис

Длинные *потока*. Статистика (*StatStg*, *StatFlag*)

## <a name="return-value"></a>Возвращаемое значение

Значение типа long, указывающее состояние операции.

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*StatStg* |Структура STATSTG, будут заполнены сведения о потоке. Реализация метода Stat объект ADO Stream не заполните все поля структуры.|
|*StatFlag* |Указывает, что этот метод не возвращает некоторые элементы в структуре STATSTG сэкономить операция выделения памяти. Значения берутся из перечисления STATFLAG.<br/><br/>Перечисление STATFLAG имеет два значения:<br/>-STATFLAG_DEFAULT: 0<br/>-STATFLAG_NONAME: 1 |


## <a name="remarks"></a>Примечания

В следующих полях структуры STATSTG заполняет версии Stat метода, реализованного в объекте ADO Stream:

|Поле|Описание|
|:--------|:----------|
|*pwcsName* |Строка, содержащая имя потока, если он доступен и StatFlag значение STATFLAG\_NONAME не указан.|
|*cbSize* |Указывает размер массива байтов или потока в байтах.|
|*mtime* |Указывает время последнего изменения для данного объекта хранилища, потока или массива байтов.|
|*CTime* |Указывает время создания для данного объекта хранилища, потока или массива байтов.|
|*atime* |Указывает время последнего обращения к этой хранилища, потока или массива байтов.|

Если STATFLAG\_NONAME указан в параметре StatFlag, имя потока не возвращается.

Если STATFLAG\_NONAME не указан в параметре StatFlag и нет имя не для текущего потока, это значение будет E\_NOTIMPL.

