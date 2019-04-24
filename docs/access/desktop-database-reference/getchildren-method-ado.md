---
title: Метод доЧернего элемента (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ca8c113a377543ea8624972adb5958612a3fc72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292309"
---
# <a name="getchildren-method-ado"></a>Метод доЧернего элемента (ADO)


**Область применения**: Access 2013, Office 2013


Возвращает объект [Recordset](recordset-object-ado.md) , в строках которого представлены дочерние элементы [записи](record-object-ado.md)коллекции.

## <a name="syntax"></a>Синтаксис

**Set** *набор записей*  =  *запись*. GetChildren

## <a name="return-value"></a>Возвращаемое значение

Объект **Recordset** , для которого каждая строка представляет дочерний объект текущей **записи** . Например, дочерние элементы **записи** , представляющей каталог, будут представлять собой файлы и подкаталоги, содержащиеся в родительском каталоге.

## <a name="remarks"></a>Замечания

Поставщик определяет, какие столбцы существуют в возвращенном **наборе записей**. Например, поставщик источника документов всегда возвращает **набор записей**ресурса.

