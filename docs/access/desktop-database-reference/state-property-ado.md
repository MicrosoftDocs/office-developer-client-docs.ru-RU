---
title: Свойство State (ADO)
TOCTitle: State property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bce3f87a6530315a128396fe0e4de5390e0f47e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722825"
---
# <a name="state-property-ado"></a>Свойство State (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает для всех объектов, которые применяются ли состояние объекта открытой или закрытой.

Указывает, что все соответствующие объекты выполнения асинхронного метода, подключение, выполнение или получение текущего состояния объекта.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **Long** , может быть [ObjectStateEnum](objectstateenum.md) значением. Значение по умолчанию — **adStateClosed**.

## <a name="remarks"></a>Замечания

Свойство **состояние** для определения текущего состояния того или иного объекта в любое время.

Свойство **состояние** объекта может содержать комбинацию значений. Например если выполняется оператор, это свойство будет иметь значение объединенный **adStateOpen** и **adStateExecuting**.

Свойство **State** доступен только для чтения.

