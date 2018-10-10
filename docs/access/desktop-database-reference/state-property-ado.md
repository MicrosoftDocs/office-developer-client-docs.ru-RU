---
title: State Property (ADO)
TOCTitle: State Property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2bde03f1d6c7619e8140248b2551002f0453fc9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483030"
---
# <a name="state-property-ado"></a>State Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает для всех объектов, которые применяются ли состояние объекта открытой или закрытой.

Указывает, что все соответствующие объекты выполнения асинхронного метода, подключение, выполнение или получение текущего состояния объекта.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **Long** , может быть [ObjectStateEnum](objectstateenum.md) значением. Значение по умолчанию — **adStateClosed**.

## <a name="remarks"></a>Замечания

Свойство **состояние** для определения текущего состояния того или иного объекта в любое время.

Свойство **состояние** объекта может содержать комбинацию значений. Например если выполняется оператор, это свойство будет иметь значение объединенный **adStateOpen** и **adStateExecuting**.

Свойство **State** доступен только для чтения.

