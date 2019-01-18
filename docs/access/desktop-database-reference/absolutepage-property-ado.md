---
title: Свойство AbsolutePage (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a0ad4caa6e31b6de39904016cd848e12690f72e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705262"
---
# <a name="absolutepage-property-ado"></a>Свойство AbsolutePage (ADO)

**Применимо к**: Access 2013, Office 2013

Указывает, на какую страницу находится текущей записи.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение типа **Long** от 1 число страниц в объекте [набора записей](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)) либо одно из значений [PositionEnum](positionenum.md) .

## <a name="remarks"></a>Замечания

Это свойство можно использовать для идентификации номер страницы, на котором расположена текущая запись. Он использует свойство [PageSize](pagesize-property-ado.md) логическое разделение строк общее число объекта **набора записей** в набор страниц, каждый из которых содержит число записей, равное **PageSize** (за исключением на последней странице, которая может быть меньше записей). Поставщик должен поддерживать соответствующие функциональные возможности для этого свойства, чтобы оно было доступно.

После получения и установки свойства **AbsolutePage** , ADO используется свойство [AbsolutePosition](absoluteposition-property-ado.md) и свойство [PageSize](pagesize-property-ado.md) вместе следующим образом:

- Для получения **AbsolutePage**ADO сначала получает **AbsolutePosition**и затем делит их **PageSize**.

- Чтобы задать **AbsolutePage**, ADO перемещает **AbsolutePosition** , как показано ниже: его умножает **PageSize** на новое значение **AbsolutePage** и затем добавляет значение 1. В результате текущую позицию в **наборе записей** после успешной установки **AbsolutePage** является первой записи в эту страницу.

Как и свойство **AbsolutePosition** **AbsolutePage** на основе 1 и имеет значение 1, если текущая запись является первой записи в **набор записей**. Задайте это свойство, чтобы перейти к первой записи определенной страницы. Получите общее число страниц из свойства **PageCount** .

