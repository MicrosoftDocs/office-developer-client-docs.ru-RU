---
title: GetString Method (ADO)
TOCTitle: GetString Method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b11ddeb5a2cffad6ef7703b04d5730b54c4949b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481314"
---
# <a name="getstring-method-ado"></a>GetString Method (ADO)


**Применимо к**: Access 2013 | Office 2013


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

