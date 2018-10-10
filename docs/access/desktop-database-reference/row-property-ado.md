---
title: Строка свойство - ActiveX Data Objects (ADO)
TOCTitle: Row Property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05d97bb411c4199677f512d9412653ca5a4b4fe1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481199"
---
# <a name="row-property-ado"></a>Row Property (ADO)


**Применимо к**: Access 2013 | Office 2013



Получает или задает объект OLE DB **строку** из/на объекте **ADORecordConstruction** . При использовании **поместить\_строки** Чтобы установить для объекта **строки** , строка включается в объект ADO **записи** . Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT get\_строки (\[out retval\] IUnknown\* \* ppRow);

Поместите HRESULT\_строки (\[в\] IUnknown\* pRow);

## <a name="parameters"></a>Параметры

  - *ppRow*

  - Указатель на объект OLE DB **строки** .

  - *PRow*

  - Объект OLE DB **строки** .

## <a name="return-values"></a>Return Values

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="applies-to"></a>Применимо к

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

