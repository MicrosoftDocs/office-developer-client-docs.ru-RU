---
title: Метод GetString (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ea28efb8fdeaa0643d1d940419b7650527ddf6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292190"
---
# <a name="getstring-method-ado"></a>Метод GetString (ADO)

**Область применения**: Access 2013, Office 2013

Возвращает набор [записей в](recordset-object-ado.md) качестве строки.

## <a name="syntax"></a>Синтаксис

*Variant*  =  *recordset*. GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)

## <a name="return-value"></a>Возвращаемое значение

Возвращает набор **записей в** качестве значения строки **Variant** (BSTR).

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*StringFormat* |Значение [StringFormatEnum,](stringformatenum.md) которое указывает, как **набор записей** должен быть преобразован в строку. Параметры *RowDelimiter,* *ColumnDelimiter* и *NullExpr* используются только с *параметром StringFormat* **adClipString.**|
|*NumRows* |Необязательный параметр. Количество строк, которые необходимо преобразовать в **наборе записей.** Если *NumRows* не указан или превышает общее число строк в наборе **recordset,** то все строки в **наборе Recordset** преобразуются.|
|*ColumnDelimiter* |Необязательный параметр. В противном случае используется разнородных столбцов, если они указаны, в противном случае символ TAB.|
|*RowDelimiter* |Необязательный параметр. В противном случае используется разность между строками, если они указаны, в противном случае символ ВОЗВРАТА КАРЕТА.|
|*NullExpr* |Необязательный параметр. Выражение, используемое в качестве значения null,если указано, в противном случае пустая строка.|

## <a name="remarks"></a>Заметки

Данные строки, но не данные схемы, сохраняются в строке. Поэтому набор **записей нельзя** повторно открыть с помощью этой строки.

Этот метод эквивалентен методу RDO **GetClipString.**

