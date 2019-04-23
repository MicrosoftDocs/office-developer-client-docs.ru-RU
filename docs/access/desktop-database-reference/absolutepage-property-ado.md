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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280686"
---
# <a name="absolutepage-property-ado"></a>Свойство AbsolutePage (ADO)

**Область применения**: Access 2013, Office 2013

Указывает, на какой странице располагается текущая запись.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Long** от 1 до числа страниц в объекте [Recordset](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)) или возвращает одно из значений [поситионенум](positionenum.md) .

## <a name="remarks"></a>Замечания

Это свойство можно использовать для определения номера страницы, на которой расположена текущая запись. Он использует свойство [pageSize](pagesize-property-ado.md) , чтобы логически разделить общее количество наборов строк объекта **Recordset** на серии страниц, каждая из которых содержит число записей, равное **pageSize** (за исключением последней страницы, которая может содержать меньше записей). Чтобы это свойство было доступно, поставщик должен поддерживать соответствующие функциональные возможности.

При извлечении или задании свойства **ABSOLUTEPAGE** ADO использует свойство [AbsolutePosition](absoluteposition-property-ado.md) и свойство [pageSize](pagesize-property-ado.md) следующим образом:

- Чтобы получить **AbsolutePage**, ADO сначала извлекает **AbsolutePosition**, а затем разделяет его на **pageSize**.

- Чтобы задать **AbsolutePage**, ADO переместит **AbsolutePosition** следующим образом: он умножает значение **pageSize** на новое значение **AbsolutePage** , а затем добавляет 1 к значению. В результате текущая позиция в **наборе записей** после успешной установки **AbsolutePage** является первой записью на этой странице.

Как и свойство **AbsolutePosition** , **AbsolutePage** имеет значение 1 и равняется 1, если текущая запись является первой записью в наборе **записей**. Задайте это свойство, чтобы перейти к первой записи определенной страницы. Получение общего числа страниц из свойства **PageCount** .

