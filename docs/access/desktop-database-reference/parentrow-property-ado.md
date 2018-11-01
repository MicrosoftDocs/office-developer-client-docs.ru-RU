---
title: Свойство ParentRow (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28f0d1c7dbc0e062ff133b9f9997f1a737c3262e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872132"
---
# <a name="parentrow-property-ado"></a>Свойство ParentRow (ADO)


**Применимо к**: Access 2013, Office 2013


Задает объект **ADORecordConstruction** контейнер объекта OLE DB **строку** , чтобы родительской строки включается в объект ADO **записи** .

Только для записи.

## <a name="syntax"></a>Синтаксис

Поместите HRESULT\_ParentRow (\[в\] IUnknown\* pParent);

## <a name="parameters"></a>Параметры

  - *pParent*

  - Контейнер для строки.

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="applies-to"></a>Применимо к

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

