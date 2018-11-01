---
title: Метод GetString (ADO)
TOCTitle: GetString Method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6c4de1278a093a1b0d4493c5dd994afe6a5d1b8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879874"
---
# <a name="getstring-method-ado"></a>Метод GetString (ADO)


**Применимо к**: Access 2013, Office 2013


Возвращает [набор записей](recordset-object-ado.md) в виде строки.

## <a name="syntax"></a>Синтаксис

*Variant* = *набора записей*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)

## <a name="return-value"></a>Возвращаемое значение

Возвращает **набор записей** как строковое значение **Variant** (BSTR).

## <a name="parameters"></a>Параметры

  - *StringFormat*

  - [StringFormatEnum](stringformatenum.md) значение, указывающее, преобразование **набора записей** к типу string. Параметры *RowDelimiter* *ColumnDelimiter*и *NullExpr* используются только с *StringFormat* из **adClipString**.

  - *NumRows*

  - Необязательный параметр. Количество строк, преобразуется в **набор записей**. Если не указан *NumRows* или больше, чем общее число строк в **набор записей**, все строки в наборе **записей** преобразуются.

  - *ColumnDelimiter*

  - Необязательный параметр. Разделитель, используемый между столбцов, если указан, в противном случае символ табуляции.

  - *RowDelimiter*

  - Необязательный параметр. Разделитель, используемый между строк, если указан, в противном случае знаков возврата каретки.

  - *NullExpr*

  - Необязательный параметр. Выражение, используется вместо значение null, если указан, в противном случае — пустая строка.

## <a name="remarks"></a>Замечания

Данные строки, но не данные схемы сохраняется в строке. Таким образом, **набор записей** не может быть открыт с помощью этой строки.

Этот метод является эквивалентом метода RDO **GetClipString** .

