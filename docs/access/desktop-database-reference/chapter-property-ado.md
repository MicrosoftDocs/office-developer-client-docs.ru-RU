---
title: Chapter Property (ADO)
TOCTitle: Chapter Property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f02b20aef2b76ff00ce23b8597132dc22b414993
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482343"
---
# <a name="chapter-property-ado"></a>Chapter Property (ADO)


**Применимо к**: Access 2013 | Office 2013
 

Получает или задает объект OLE DB **главы** из/на объекте **ADORecordsetConstruction** . При использовании **поместить\_главы** Чтобы установить для объекта **главы** , подмножество строк превращается в объект ADO **Recordset** . Это задание текущей главы из объекта **набора записей** . Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT get\_главы (\[out retval\] длинные\* plChapter);

Поместите HRESULT\_главы (\[в\] длинные lChapter);

## <a name="parameters"></a>Параметры

  - *plChapter*

  - Указатель на дескриптор главы.

  - *LChapter*

  - Дескриптор главы.

## <a name="return-values"></a>Return Values

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="applies-to"></a>Применимо к

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

