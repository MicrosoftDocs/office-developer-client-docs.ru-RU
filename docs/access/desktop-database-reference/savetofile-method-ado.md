---
title: Метод SaveToFile (ADO)
TOCTitle: SaveToFile method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f3b08c9df435c7ce995a40af7b8ad5466b79245d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706543"
---
# <a name="savetofile-method-ado"></a>Метод SaveToFile (ADO)

**Применимо к**: Access 2013, Office 2013

Сохраняет двоичные содержимое [потока](stream-object-ado.md) в файл.

## <a name="syntax"></a>Синтаксис

*Поток*. SaveToFile*имя файла*, *SaveOptions*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*FileName* |**Строковое** значение, которое содержит полное имя файла, в котором будет сохранен содержимое **потока** . Поддерживается сохранение в любое допустимое локальное местоположение или любого расположения у вас есть доступ с помощью значения UNC.|
|*SaveOptions* |[SaveOptionsEnum](saveoptionsenum.md) значение, указывающее, следует ли создавать новый файл с **SaveToFile**, если он еще не существует. Значение по умолчанию — **adSaveCreateNotExists**. С помощью этих параметров можно указать, что, если указанный файл не существует, возникает ошибка. Также можно указать, что **SaveToFile** перезаписывает текущий содержимое существующего файла.|

> [!NOTE]
> При перезаписи существующего файла (если установлено **adSaveCreateOverwrite** ) **SaveToFile** ограничивает длину любой байтов из исходного существующий файл, следующие новые [EOS](eos-property-ado.md).

## <a name="remarks"></a>Замечания

**SaveToFile** могут быть использованы для копирования содержимого объекта **потока** в локальный файл. Нет никаких изменений в содержимое или свойства объекта **потока** . Прежде чем вызывать **SaveToFile**объект **Stream** необходимо открыть.

Этот метод не изменяет сопоставления на объект **Stream** ее базовому источнику. По-прежнему будет связан с исходный URL-адрес или **запись** , которая была источника при открытии объект **Stream** .

После выполнения операции **SaveToFile** текущей позиции ([положение](position-property-ado.md)) в потоке задано значение начала потока (0).

