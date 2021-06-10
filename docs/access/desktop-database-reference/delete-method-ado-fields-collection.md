---
title: Метод удаления (коллекция полей ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294108"
---
# <a name="delete-method-ado-fields-collection"></a>Метод удаления (коллекция полей ADO)

**Область применения**: Access 2013, Office 2013


Удаляет объект из коллекции [Fields.](fields-collection-ado.md)

## <a name="syntax"></a>Синтаксис

*Поля*. Удаление *поля*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Field* |Вариант, который обозначает удаление [объекта Field.](field-object-ado.md)  Этот параметр может быть именем объекта **Field** или расположением самого **объекта Field.**|

## <a name="remarks"></a>Примечания

Вызов метода **Fields.Delete** в открытом [наборе записей](recordset-object-ado.md) вызывает ошибку во время работы.

