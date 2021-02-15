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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308927"
---
# <a name="savetofile-method-ado"></a>Метод SaveToFile (ADO)

**Область применения**: Access 2013, Office 2013

Сохраняет двоичное содержимое [Stream](stream-object-ado.md) в файл.

## <a name="syntax"></a>Синтаксис

*Stream*. SaveToFile *FileName*, *SaveOptions*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*FileName* |**Строка,** содержаная полное имя файла, в котором будет сохранено содержимое **stream.** Вы можете сохранить его в любом допустимом локальном расположении или любом расположении, к который у вас есть доступ, с помощью ЗНАЧЕНИЯ UNC.|
|*SaveOptions* |Значение [SaveOptionsEnum,](saveoptionsenum.md) которое указывает, следует ли создать новый файл с помощью **SaveToFile,** если он еще не существует. Значение по **умолчанию— adSaveCreateNotExists.** С помощью этих параметров можно указать, что ошибка возникает, если указанный файл не существует. Можно также указать, **что SaveToFile** переописает текущее содержимое существующего файла.|

> [!NOTE]
> При перезаписи существующего файла (если **установлено adSaveCreateOverwrite),** **SaveToFile** укоревает все bytes из исходного существующего файла, который следует за новой [EOS](eos-property-ado.md).

## <a name="remarks"></a>Заметки

**SaveToFile** можно использовать для копирования содержимого объекта **Stream** в локальный файл. Содержимое или свойства объекта **Stream** не изменяются. Объект **Stream** должен быть открыт перед вызовом **SaveToFile.**

Этот метод не меняет связь объекта **Stream** с его исходным источником. Объект **Stream** по-прежнему будет связан с исходным URL-адресом **или** записью, которая была его источником при открытом.

После операции **SaveToFile** текущее положение [(позиция)](position-property-ado.md)в потоке устанавливается в начале потока (0).

