---
title: Метод GetChildren (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ca8c113a377543ea8624972adb5958612a3fc72
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722027"
---
# <a name="getchildren-method-ado"></a>Метод GetChildren (ADO)


**Применимо к**: Access 2013, Office 2013


Возвращает [набор записей](recordset-object-ado.md) , строки представляют дочерние элементы коллекции [записи](record-object-ado.md).

## <a name="syntax"></a>Синтаксис

**Установка** *набор записей*  =  *записи*. GetChildren

## <a name="return-value"></a>Возвращаемое значение

Объект **набора записей** , для которой каждая строка представляет дочернего объекта **записи** . Например потомки **записи** , которая представляет каталог будет файлов и вложенных папок, содержащихся в родительской папке.

## <a name="remarks"></a>Замечания

Поставщик определяет, какие столбцы существуют в возвращаемых **записей**. Например поставщик источника документов всегда возвращает ресурсов **набора записей**.

