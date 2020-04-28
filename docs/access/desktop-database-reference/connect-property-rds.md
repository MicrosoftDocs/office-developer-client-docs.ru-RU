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

Указывает имя базы данных, из которой выполняются операции запроса и обновления.

Свойство **Connect** можно задать во время создания в службе [RDS. Объектные теги объекта DataObject или](datacontrol-object-rds.md) во время выполнения в коде сценария (например, на языке VBScript).

## <a name="syntax"></a>Синтаксис

Время конструирования \<: param Name = "Connect" value = "ConnectionString"\>

Время выполнения: Control. Connect = "ConnectionString"

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ConnectionString* |Допустимая строка подключения. Более общие сведения о строках подключения приведены в статье свойство [ConnectionString](connectionstring-property-ado.md) или документации поставщика.<br/><br/>**Note**: указание MS Remote в качестве поставщика для **RDS. Элемент управления** "объект" создает сценарий из четырех уровней. Сценарии с более чем тремя уровнями не тестировались и не должны быть необходимыми.|
|*DataControl* |Объектная переменная, представляющая **RDS. Объект управления** DataObject.|

