---
title: Подключение (RDS)
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
# <a name="connect-property-rds"></a>Подключение (RDS)

**Область применения**: Access 2013, Office 2013

Указывает имя базы данных, из которого запускаются операции запроса и обновления.

Вы можете задать **Подключение** в момент разработки в [RDS. Объектные теги объекта DataControl](datacontrol-object-rds.md) или во время запуска в коде скриптов (например, VBScript).

## <a name="syntax"></a>Синтаксис

Время разработки: \< PARAM NAME="Подключение" VALUE="ConnectionString"\>

Время запуска: DataControl. Подключение = "ConnectionString"

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ConnectionString* |Допустимая строка подключения. Дополнительные сведения о строках подключения см. в свойстве [ConnectionString](connectionstring-property-ado.md) или документации поставщика.<br/><br/>**ПРИМЕЧАНИЕ.** Указание ms Remote в качестве поставщика для **RDS. DataControl** создаст четырехуровневый сценарий. Сценарии с более чем тремя уровнями не были протестированы и не должны быть необходимы.|
|*DataControl* |Переменная объекта, представляюая **RDS. Объект DataControl.**|

