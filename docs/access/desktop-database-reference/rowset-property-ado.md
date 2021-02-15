---
title: Свойство Rowset (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306743"
---
# <a name="rowset-property-ado"></a>Свойство Rowset (ADO)

**Область применения**: Access 2013, Office 2013

Получает или задает объект OLE DB **Rowset** из/объекта **ADORecordsetConstruction.** При использовании put \_ Rowset набор строк превращается в объект ADO **Recordset.**

Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT get \_ Rowset( \[ out, retval \] IUnknown \* \* ppRowset);

HRESULT put \_ Rowset( \[ in \] IUnknown \* pRowset);

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ppRowset* |Указатель на объект **rowset** OLE DB.|
|*PRowset* |Объект OLE DB **Rowset.**|

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойства возвращает стандартные значения HRESULT, включая S \_ OK и E \_ FAIL.

## <a name="applies-to"></a>Область применения

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

