---
title: Свойство RowPosition (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0adb1cdf9ce7b096d7b80b86a89a819d5789b60b
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949385"
---
# <a name="rowposition-property-ado"></a>Свойство RowPosition (ADO)

**Применимо к**: Access 2013, Office 2013

Получает или задает объект OLE DB **RowPosition** из/на объекте **ADORecordsetConstruction** . При использовании **поместить\_RowPosition** Чтобы установить для объекта **RowPosition** , объекте результирующего **набора записей** использует объект **RowPosition** для определения текущей строки.

Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT get\_RowPosition (\[out retval\] IUnknown\* \* ppRowPos);

Поместите HRESULT\_RowPosition (\[в\] IUnknown\* pRowPos);

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ppRowPos* |Указатель на объект OLE DB **RowPosition** .|
|*PRowPos* |Объект OLE DB **RowPosition** .|

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="remarks"></a>Примечания

Если значение этого свойства, если объекта **набора записей** в объекте **RowPosition** отличается от объекта **набора записей** в объекте **набора записей** , бывшие переопределяет второй. То же самое относится к текущей **главы** **RowPosition** также.

## <a name="applies-to"></a>Область применения

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

