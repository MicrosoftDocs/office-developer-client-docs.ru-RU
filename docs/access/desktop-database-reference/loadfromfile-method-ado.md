---
title: Метод LoadFromFile (ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9316bc4302a559fa44082a0576595707157e9d64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289887"
---
# <a name="loadfromfile-method-ado"></a>Метод LoadFromFile (ADO)

**Область применения**: Access 2013, Office 2013

Загружает содержимое существующего файла в [поток.](stream-object-ado.md)

## <a name="syntax"></a>Синтаксис

*Stream*. LoadFromFile *FileName*

## <a name="parameters"></a>Параметры

|Имя |Описание|
|:----|:----------|
|*FileName* |**Строка** с именем файла, загружаемого в **поток.** *FileName может* содержать любой допустимый путь и имя в формате UNC. Если указанный файл не существует, возникает ошибка времени запуска.|

## <a name="remarks"></a>Заметки

Этот метод можно использовать для загрузки содержимого локального файла в объект **Stream.** Это может использоваться для отправки содержимого локального файла на сервер.

Объект **Stream** должен быть уже открыт перед вызовом **LoadFromFile.** Этот метод не меняет привязку объекта **Stream;** Он будет по-прежнему привязан к объекту, указанному  URL-адресом или записью, с помощью которой был изначально открыт Stream. 

**LoadFromFile** перезаписает текущее содержимое объекта **Stream** данными, считаными из файла. Все существующие в **потоке** bytes перезаписываются содержимым файла. Все ранее существовавшиеся и оставшиеся в соответствии с [EOS,](eos-property-ado.md) созданные **LoadFromFile,** усечены.

После вызова **LoadFromFile** текущая позиция устанавливается в начале **потока** [(позиция](position-property-ado.md) — 0).

Так как в начало потока для кодии может быть добавлено 2 файла, размер потока может не совпадать с размером файла, из которого он был загружен.

