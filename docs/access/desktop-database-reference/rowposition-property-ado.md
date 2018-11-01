---
title: Свойство RowPosition (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f83d1b113b29be06ffded5263791d3db3068f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869073"
---
# <a name="rowposition-property-ado"></a>Свойство RowPosition (ADO)


**Применимо к**: Access 2013, Office 2013



Получает или задает объект OLE DB **RowPosition** из/на объекте **ADORecordsetConstruction** . При использовании **поместить\_RowPosition** Чтобы установить для объекта **RowPosition** , объекте результирующего **набора записей** использует объект **RowPosition** для определения текущей строки.

Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT get\_RowPosition (\[out retval\] IUnknown\* \* ppRowPos);

Поместите HRESULT\_RowPosition (\[в\] IUnknown\* pRowPos);

## <a name="parameters"></a>Параметры

  - *ppRowPos*

  - Указатель на объект OLE DB **RowPosition** .

  - *PRowPos*

  - Объект OLE DB **RowPosition** .

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="remarks"></a>Замечания

Если значение этого свойства, если объекта **набора записей** в объекте **RowPosition** отличается от объекта **набора записей** в объекте **набора записей** , бывшие переопределяет второй. То же самое относится к текущей **главы** **RowPosition** также.

## <a name="applies-to"></a>Применимо к

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

