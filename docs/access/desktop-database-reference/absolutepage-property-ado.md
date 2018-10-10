---
title: AbsolutePage Property (ADO)
TOCTitle: AbsolutePage Property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 60b7b58efaa6fb8686e4f43da9b9733f3629f1a7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482141"
---
# <a name="absolutepage-property-ado"></a>AbsolutePage Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает, на какую страницу находится текущей записи.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение типа **Long** от 1 число страниц в объекте [набора записей](recordset-object-ado.md) ( [PageCount](pagecount-property-ado.md) ) либо одно из значений [PositionEnum](positionenum.md) .

## <a name="remarks"></a>Замечания

Это свойство можно использовать для идентификации номер страницы, на котором расположена текущая запись. Он использует свойство [PageSize](pagesize-property-ado.md) логическое разделение строк общее число объекта **набора записей** в набор страниц, каждый из которых содержит число записей, равное **PageSize** (за исключением на последней странице, которая может быть меньше записей). Поставщик должен поддерживать соответствующие функциональные возможности для этого свойства, чтобы оно было доступно.

После получения и установки свойства **AbsolutePage** , ADO используется свойство [AbsolutePosition](absoluteposition-property-ado.md) и свойство [PageSize](pagesize-property-ado.md) вместе следующим образом:

  - Для получения **AbsolutePage**ADO сначала получает **AbsolutePosition**и затем делит их **PageSize**.

  - Чтобы задать **AbsolutePage**, ADO перемещает **AbsolutePosition** , как показано ниже: его умножает **PageSize** на новое значение **AbsolutePage** и затем добавляет значение 1. В результате будет текущую позицию в **наборе записей** после успешной установки **AbsolutePage** первой записи в эту страницу.

Как и свойство **AbsolutePosition** **AbsolutePage** на основе 1 и имеет значение 1, если текущая запись является первой записи в **набор записей**. Задайте это свойство, чтобы перейти к первой записи определенной страницы. Получите общее число страниц из свойства **PageCount** .

