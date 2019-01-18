---
title: Строка свойство - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715006"
---
# <a name="row-property-ado"></a>Свойство Row (ADO)

**Применимо к**: Access 2013, Office 2013

Получает или задает объект OLE DB **строку** из/на объекте **ADORecordConstruction** . При использовании **поместить\_строки** Чтобы установить для объекта **строки** , строка включается в объект ADO **записи** . Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT get\_строки (\[out retval\] IUnknown\* \* ppRow);

Поместите HRESULT\_строки (\[в\] IUnknown\* pRow);

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*ppRow* |Указатель на объект OLE DB **строки** .|
|*PRow* |Объект OLE DB **строки** .|

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="applies-to"></a>Область применения

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

