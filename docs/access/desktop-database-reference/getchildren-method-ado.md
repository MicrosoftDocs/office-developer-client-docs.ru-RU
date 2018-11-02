---
title: Метод GetChildren (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcc687e5151e95d61939c30aa4c6be4063b67c47
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931269"
---
# <a name="getchildren-method-ado"></a>Метод GetChildren (ADO)


**Применимо к**: Access 2013, Office 2013


Возвращает [набор записей](recordset-object-ado.md) , строки представляют дочерние элементы коллекции [записи](record-object-ado.md).

## <a name="syntax"></a>Синтаксис

**Установка** *набор записей*  =  *записи*. GetChildren

## <a name="return-value"></a>Возвращаемое значение

Объект **набора записей** , для которой каждая строка представляет дочернего объекта **записи** . Например потомки **записи** , которая представляет каталог будет файлов и вложенных папок, содержащихся в родительской папке.

## <a name="remarks"></a>Примечания

Поставщик определяет, какие столбцы существуют в возвращаемых **записей**. Например поставщик источника документов всегда возвращает ресурсов **набора записей**.

