---
title: Свойство URL-адрес (RDS - ссылки для настольных баз данных Access)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aafc8cc10410cafed21e38ad7fec269c391c1fa2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702392"
---
# <a name="url-property-rds"></a>Свойство URL (RDS)

**Применимо к**: Access 2013, Office 2013

Указывает строку, которая содержит относительный или абсолютный URL-адрес.

Можно задать свойство **URL-адреса** в тег OBJECT объекта [DataControl](datacontrol-object-rds.md) во время разработки или во время выполнения в код сценария.

## <a name="syntax"></a>Синтаксис

Время разработки: \<параметров имя = значение «URL-адрес» = «Сервер»\>

Во время выполнения: DataControl.URL="Server»

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Server* |**Строковое** значение, содержащее допустимый URL-адрес.|
|*DataControl* |Объектная переменная, которая представляет собой объект- **DataControl** .|

## <a name="remarks"></a>Замечания

Как правило URL-адрес указывает файл страницы Active Server (.asp), который может создавать и возвращать [набора записей](recordset-object-ado.md). Таким образом пользователь может получить **записей** без вызова объекта [DataFactory](datafactory-object-rdsserver.md) на сервере или программа настраиваемый бизнес-объект.

Если свойство **URL-адрес** [SubmitChanges](submitchanges-method-rds.md) будет внесения изменений в расположении, указанном URL-адрес.

