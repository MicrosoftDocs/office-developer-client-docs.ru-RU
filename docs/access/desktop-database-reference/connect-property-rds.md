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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295984"
---
# <a name="connect-property-rds"></a>Свойство Connect (RDS)

**Область применения**: Access 2013, Office 2013

Указывает имя базы данных, из которой запускаются операции запроса и обновления.

Вы можете настроить свойство **Connect** во время разработки в [RDS. Теги](datacontrol-object-rds.md) OBJECT объекта DataControl или во время запуска в коде скриптов (например, VBScript).

## <a name="syntax"></a>Синтаксис

Время разработки: \< PARAM NAME="Connect" VALUE="ConnectionString"\>

Время запуска: DataControl.Connect = "ConnectionString"

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ConnectionString* |Допустимая строка подключения. Дополнительные общие сведения о строках подключений см. в свойстве [ConnectionString](connectionstring-property-ado.md) или документации поставщика.<br/><br/>**ПРИМЕЧАНИЕ.** Указание MS Remote в качестве поставщика **для RDS. DataControl** создаст четырехуровневый сценарий. Сценарии более трех уровней не были протестированы и не нужны.|
|*DataControl* |Объектная переменная, представляюная **RDS. Объект DataControl.**|

