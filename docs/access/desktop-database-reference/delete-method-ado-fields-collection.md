---
title: Удаление метода (коллекции полей ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b33c15adf1d079e2da12590891d950aa35e5414f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950178"
---
# <a name="delete-method-ado-fields-collection"></a>Удаление метода (коллекции полей ADO)

**Применимо к**: Access 2013, Office 2013


Удаляет объект из коллекции [полей](fields-collection-ado.md) .

## <a name="syntax"></a>Синтаксис

*Поля*. Удаление*поля*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Поле* |**Variant** , который определяет удаляемый объект [поля](field-object-ado.md) . Этот параметр может быть имя объекта **поля** или порядковый номер самого объекта **поля** .|

## <a name="remarks"></a>Примечания

Вызов метода **Fields.Delete** для открытия [набора записей](recordset-object-ado.md) вызывает ошибку времени выполнения.

