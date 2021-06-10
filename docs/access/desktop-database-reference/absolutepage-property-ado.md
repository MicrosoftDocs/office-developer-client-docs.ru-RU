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

Указывает, на какой странице находится текущая запись.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Long** от 1 до количества страниц в объекте [Recordset](recordset-object-ado.md) [(PageCount)](pagecount-property-ado.md)или возвращает одно из [значений PositionEnum.](positionenum.md)

## <a name="remarks"></a>Примечания

Это свойство можно использовать для определения номера страницы, на котором расположена текущая запись. Свойство [PageSize](pagesize-property-ado.md) логически делит общее число строк объекта **Recordset** на ряд страниц, каждая из которых имеет количество записей, равное **PageSize** (за исключением последней страницы, записей может быть меньше). Поставщик должен поддерживать соответствующие функции, чтобы это свойство было доступно.

При получении или настройке **свойства AbsolutePage** ADO использует свойство [AbsolutePosition](absoluteposition-property-ado.md) и [свойство PageSize](pagesize-property-ado.md) следующим образом:

- Чтобы получить **AbsolutePage,** ADO сначала извлекает **AbsolutePosition,** а затем делит его на **PageSize.**

- Чтобы установить **AbsolutePage,** ADO перемещает **AbsolutePosition** следующим образом: она умножает **PageSize** на новое значение **AbsolutePage** и добавляет 1 к значению. В результате текущее положение в **Наборе записей** после успешного установки **AbsolutePage** является первой записью на этой странице.

Как и **свойство AbsolutePosition,** **AbsolutePage** основан на 1 и равен 1, когда текущая запись является первой записью в **Наборе записей.** Установите это свойство, чтобы перейти к первой записи определенной страницы. Получение общего числа страниц из свойства **PageCount.**

