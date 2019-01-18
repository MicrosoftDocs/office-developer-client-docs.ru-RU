---
title: Свойство Connect (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42e7dd643985cee9aef8887099eb90dcdb381f4e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706739"
---
# <a name="connect-property-rds"></a>Свойство Connect (RDS)

**Применимо к**: Access 2013, Office 2013

Указывает имя базы данных, из которой запускаются операций запросов и обновления.

Можно задать свойство **подключение** во время разработки в [RDS. DataControl](datacontrol-object-rds.md) теги OBJECT объекта, или во время выполнения в коде (например, VBScript) сценария.

## <a name="syntax"></a>Синтаксис

Время разработки: \<параметров имя = значение «связь» = «ConnectionString»\>

Во время выполнения: DataControl.Connect = «ConnectionString»

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*ConnectionString* |Это допустимая строка подключения. Более общие сведения о строках подключения отображаться со значением свойства [ConnectionString](connectionstring-property-ado.md) или документации поставщика.<br/><br/>**Примечание**: Указание удаленного MS в качестве поставщика для **RDS. DataControl** бы создать сценарий четыре уровня. Сценарии, больше, чем три уровня не проверялись и не должно быть необходимым.|
|*DataControl* |Объектную переменную, которая представляет **RDS. DataControl** объекта.|

