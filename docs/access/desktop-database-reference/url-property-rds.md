---
title: Свойство URL (RDS — доступ к настольной базе данных)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aafc8cc10410cafed21e38ad7fec269c391c1fa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313400"
---
# <a name="url-property-rds"></a>Свойство URL(RDS)

**Область применения**: Access 2013, Office 2013

Указывает строку, содержаную относительный или абсолютный URL-адрес.

Свойство **URL-адреса** можно установить во время разработки в теге OBJECT объекта [DataControl](datacontrol-object-rds.md) или во время запуска в коде скриптов.

## <a name="syntax"></a>Синтаксис

Время разработки: \< PARAM NAME="URL"VALUE="Server"\>

Время запуска: DataControl.URL="Server"

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Server* |Значение **String,** содержа которое содержит допустимый URL-адрес.|
|*DataControl* |Переменная объекта, представляют **объект DataControl.**|

## <a name="remarks"></a>Примечания

Как правило, URL-адрес определяет файл Active Server Page (.asp), который может создавать и возвращать [набор записей.](recordset-object-ado.md) Таким образом, пользователь может получить **Набор записей,** не вызывая серверный объект [DataFactory](datafactory-object-rdsserver.md) или запрограммировать настраиваемый бизнес-объект.

Если свойство **URL-адреса** задано, [SubmitChanges](submitchanges-method-rds.md) будет отправлять изменения в указанное URL-адресом расположение.

