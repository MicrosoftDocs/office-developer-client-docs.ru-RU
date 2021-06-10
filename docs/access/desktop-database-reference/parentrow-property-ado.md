---
title: Свойство ParentRow (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287740"
---
# <a name="parentrow-property-ado"></a>Свойство ParentRow (ADO)

**Область применения**: Access 2013, Office 2013

Задает контейнер объекта OLE DB **Row** на объект **ADORecordConstruction,** чтобы родитель строки превратился в объект записи **ADO.**

Только для записи.

## <a name="syntax"></a>Синтаксис

HRESULT put \_ ParentRow \[ (in \] IUnknown \* pParent);

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*pParent* |Контейнер строки.|

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойства возвращает стандартные значения HRESULT, в том числе S \_ OK и E \_ FAIL.

## <a name="applies-to"></a>Область применения

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

