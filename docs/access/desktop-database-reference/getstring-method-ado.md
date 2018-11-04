---
title: Метод GetString (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b4926b3568d6c7289ca9d3158a8723e016ed344
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949675"
---
# <a name="getstring-method-ado"></a>Метод GetString (ADO)

**Применимо к**: Access 2013, Office 2013

Возвращает [набор записей](recordset-object-ado.md) в виде строки.

## <a name="syntax"></a>Синтаксис

*Variant* = *набора записей*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)

## <a name="return-value"></a>Возвращаемое значение

Возвращает **набор записей** как строковое значение **Variant** (BSTR).

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*StringFormat* |[StringFormatEnum](stringformatenum.md) значение, указывающее, преобразование **набора записей** к типу string. Параметры *RowDelimiter* *ColumnDelimiter*и *NullExpr* используются только с *StringFormat* из **adClipString**.|
|*NumRows* |Необязательно указывать. Количество строк, преобразуется в **набор записей**. Если не указан *NumRows* или больше, чем общее число строк в **набор записей**, все строки в наборе **записей** преобразуются.|
|*ColumnDelimiter* |Необязательно указывать. Разделитель, используемый между столбцов, если указан, в противном случае символ табуляции.|
|*RowDelimiter* |Необязательно указывать. Разделитель, используемый между строк, если указан, в противном случае знаков возврата каретки.|
|*NullExpr* |Необязательно указывать. Выражение, используется вместо значение null, если указан, в противном случае — пустая строка.|

## <a name="remarks"></a>Примечания

Данные строки, но не данные схемы сохраняется в строке. Таким образом, **набор записей** не может быть открыт с помощью этой строки.

Этот метод является эквивалентом метода RDO **GetClipString** .

