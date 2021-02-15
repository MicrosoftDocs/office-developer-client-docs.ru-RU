---
title: Метод Stat — ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308553"
---
# <a name="stat-method-ado"></a>Метод Stat (ADO)

**Область применения**: Access 2013, Office 2013

Извлекает сведения об **объекте Stream.**

## <a name="syntax"></a>Синтаксис

Длинный *поток.* Stat(*StatStg*, *StatFlag*)

## <a name="return-value"></a>Возвращаемое значение

Длинное значение, указывающее состояние операции.

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*StatStg* |Структура STATSTG, которая будет заполнена сведениями о потоке. Реализация метода Stat, используемого объектом ADO Stream, не заполняет все поля структуры.|
|*StatFlag* |Указывает, что этот метод не возвращает некоторые члены в структуре STATSTG, тем самым экономя операцию выделения памяти. Значения принимаются из enumeration STATFLAG.<br/><br/>В значении STATFLAG есть два значения:<br/>- STATFLAG_DEFAULT: 0<br/>- STATFLAG_NONAME: 1 |


## <a name="remarks"></a>Заметки

Версия метода Stat, реализованного для объекта ADO Stream, заполняется в следующих полях структуры STATSTG:

|Поле|Описание|
|:--------|:----------|
|*pwcsName* |Строка, содержащая имя потока, если он доступен и значение StatFlag STATFLAG \_ NONAME не указано.|
|*cbSize* |Указывает размер массива байтов или потока в байтах.|
|*mtime* |Указывает время последнего изменения для данного объекта хранилища, потока или массива байтов.|
|*ctime* |Указывает время создания для данного объекта хранилища, потока или массива байтов.|
|*atime* |Указывает время последнего доступа к этому хранилищу, потоку или массиву byte.|

Если параметр STATFLAG NONAME указан в параметре \_ StatFlag, имя потока не возвращается.

Если параметр STATFLAG NONAME не указан в параметре StatFlag и имя для текущего потока не доступно, это значение будет \_ иметь значение E \_ NOTIMPL.

