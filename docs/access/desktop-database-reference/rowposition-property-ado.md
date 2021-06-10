---
title: Свойство RowPosition (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306862"
---
# <a name="rowposition-property-ado"></a>Свойство RowPosition (ADO)

**Область применения**: Access 2013, Office 2013

Получает или задает объект OLE DB **RowPosition** из/на **объект ADORecordsetConstruction.** При использовании **put \_ RowPosition** для определения объекта **RowPosition** в результате объект **Recordset** использует объект **RowPosition** для определения текущей строки.

Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT get \_ RowPosition \[ (out, retval \] IUnknown \* \* ppRowPos);

HRESULT put \_ RowPosition \[ (in \] IUnknown \* pRowPos);

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ppRowPos* |Указатель на объект **RowPosition** OLE DB.|
|*PRowPos* |Объект **RowPosition** OLE DB.|

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойства возвращает стандартные значения HRESULT, в том числе S \_ OK и E \_ FAIL.

## <a name="remarks"></a>Примечания

Если это свойство задано, если объект **Rowset** на объекте **RowPosition** отличается от объекта Rowset на объекте **Recordset,** первый переопределит последнее.  То же самое относится и к текущей **главе** **RowPosition.**

## <a name="applies-to"></a>Область применения

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

