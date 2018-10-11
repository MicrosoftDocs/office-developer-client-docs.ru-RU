---
title: GetChildren Method (ADO)
TOCTitle: GetChildren Method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a11f3e34f8dcb45bab88d8ff87e69067103e4640
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480293"
---
# <a name="getchildren-method-ado"></a>GetChildren Method (ADO)


**Применимо к**: Access 2013 | Office 2013


Возвращает [набор записей](recordset-object-ado.md) , строки представляют дочерние элементы коллекции [записи](record-object-ado.md).

## <a name="syntax"></a>Синтаксис

**Установка** *набор записей*  =  *записи*. GetChildren

## <a name="return-value"></a>Возвращаемое значение

Объект **набора записей** , для которой каждая строка представляет дочернего объекта **записи** . Например потомки **записи** , которая представляет каталог будет файлов и вложенных папок, содержащихся в родительской папке.

## <a name="remarks"></a>Замечания

Поставщик определяет, какие столбцы существуют в возвращаемых **записей**. Например поставщик источника документов всегда возвращает ресурсов **набора записей**.

