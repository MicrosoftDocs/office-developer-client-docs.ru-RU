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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720963"
---
# <a name="rowposition-property-ado"></a>Свойство RowPosition (ADO)

**Применимо к**: Access 2013, Office 2013

Получает или задает объект OLE DB **RowPosition** из/на объекте **ADORecordsetConstruction** . При использовании **поместить\_RowPosition** Чтобы установить для объекта **RowPosition** , объекте результирующего **набора записей** использует объект **RowPosition** для определения текущей строки.

Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT get\_RowPosition (\[out retval\] IUnknown\* \* ppRowPos);

Поместите HRESULT\_RowPosition (\[в\] IUnknown\* pRowPos);

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*ppRowPos* |Указатель на объект OLE DB **RowPosition** .|
|*PRowPos* |Объект OLE DB **RowPosition** .|

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="remarks"></a>Замечания

Если значение этого свойства, если объекта **набора записей** в объекте **RowPosition** отличается от объекта **набора записей** в объекте **набора записей** , бывшие переопределяет второй. То же самое относится к текущей **главы** **RowPosition** также.

## <a name="applies-to"></a>Область применения

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

