---
title: Свойство Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7523a930feed7431bf8be0bbb7222a4b305483
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949399"
---
# <a name="chapter-property-ado"></a>Свойство Chapter (ADO)

**Применимо к**: Access 2013, Office 2013
 
Получает или задает объект OLE DB **главы** из/на объекте **ADORecordsetConstruction** . При использовании **поместить\_главы** Чтобы установить для объекта **главы** , подмножество строк превращается в объект ADO **Recordset** . Это задание текущей главы из объекта **набора записей** . Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT get\_главы (\[out retval\] длинные\* plChapter);

Поместите HRESULT\_главы (\[в\] длинные lChapter);

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*plChapter* |Указатель на дескриптор главы.|
|*LChapter* |Дескриптор главы.|

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="applies-to"></a>Применимо к

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

