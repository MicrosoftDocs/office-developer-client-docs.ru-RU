---
title: RowPosition Property (ADO)
TOCTitle: RowPosition Property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a4512157e70f4f5a7533e2a480dd96aa3693741
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480648"
---
# <a name="rowposition-property-ado"></a>RowPosition Property (ADO)


**Применимо к**: Access 2013 | Office 2013



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

## <a name="return-values"></a>Return Values

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="remarks"></a>Замечания

Если значение этого свойства, если объекта **набора записей** в объекте **RowPosition** отличается от объекта **набора записей** в объекте **набора записей** , бывшие переопределяет второй. То же самое относится к текущей **главы** **RowPosition** также.

## <a name="applies-to"></a>Применимо к

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

