---
title: Удаление метода (коллекции полей ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718261"
---
# <a name="delete-method-ado-fields-collection"></a>Удаление метода (коллекции полей ADO)

**Применимо к**: Access 2013, Office 2013


Удаляет объект из коллекции [полей](fields-collection-ado.md) .

## <a name="syntax"></a>Синтаксис

*Поля*. Удаление*поля*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Поле* |**Variant** , который определяет удаляемый объект [поля](field-object-ado.md) . Этот параметр может быть имя объекта **поля** или порядковый номер самого объекта **поля** .|

## <a name="remarks"></a>Замечания

Вызов метода **Fields.Delete** для открытия [набора записей](recordset-object-ado.md) вызывает ошибку времени выполнения.

