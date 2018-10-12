---
title: CompareBookmarks Method (ADO)
TOCTitle: CompareBookmarks Method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd6949c74e27cfb961b2a8731030b0af3b14ceb8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480370"
---
# <a name="comparebookmarks-method-ado"></a>CompareBookmarks Method (ADO)


**Применимо к**: Access 2013 | Office 2013

Сравнение двух закладки и возвращает сведения об их значения.

## <a name="syntax"></a>Синтаксис

*результат* = *набора записей*. CompareBookmarks (*Bookmark1*, *Bookmark2*)

## <a name="return-value"></a>Возвращаемое значение

Возвращает [CompareEnum](compareenum.md) значение, указывающее положение относительно строки из двух записей, представленное закладок.

## <a name="parameters"></a>Параметры

  - *Bookmark1*

  - Закладка первой строки.

  - *Bookmark2*

  - Закладка второй строке.

## <a name="remarks"></a>Замечания

Закладки необходимо установить на тот же объект [набора записей](recordset-object-ado.md) или объекта **набора записей** и его [копия](clone-method-ado.md). Сравнение надежно закладок из разных объектов **набора записей** , даже в том случае, если они были созданы на основе команду или источника. Ни сравнение закладки для объекта **набора записей** , основной поставщик не поддерживает сравнения.

Закладка уникально идентифицирует строки в объекте **набора записей** . Свойство [закладку](bookmark-property-ado.md) текущей строки используется для получения ее закладки.

Так как тип данных закладки зависит от поставщика, ADO представляет его как переменную типа Variant. К примеру, закладки SQL Server имеют тип DBTYPE\_R8 (Double). ADO предоставить этот тип в качестве типа Variant с подтипом типа Double.

При сравнении закладки, ADO не пытается любого типа приведения. Значения, просто передаются в поставщик где происходит сравнить. Если закладки, переданной в метод **CompareBookmarks** хранятся в переменных различных типов, его можно создать ошибка type mismatch «Аргументы имеют неправильный тип, находятся вне допустимого диапазона или конфликтуют друг с другом.»

Закладки, который не является допустимым или неправильно сформированные приведет к ошибке.
