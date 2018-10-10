---
title: ParentRow Property (ADO)
TOCTitle: ParentRow Property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 834dcaed7d1acdcf66410584436e2ccee8c91c56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483248"
---
# <a name="parentrow-property-ado"></a>ParentRow Property (ADO)


**Применимо к**: Access 2013 | Office 2013


Задает объект **ADORecordConstruction** контейнер объекта OLE DB **строку** , чтобы родительской строки включается в объект ADO **записи** .

Только для записи.

## <a name="syntax"></a>Синтаксис

Поместите HRESULT\_ParentRow (\[в\] IUnknown\* pParent);

## <a name="parameters"></a>Параметры

  - *pParent*

  - Контейнер для строки.

## <a name="return-values"></a>Return Values

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="applies-to"></a>Применимо к

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

