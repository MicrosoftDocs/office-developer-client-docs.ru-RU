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

*Stream*. Имя файла LoadFromFile 

## <a name="parameters"></a>Параметры

|Имя |Описание|
|:----|:----------|
|*FileName* |Значение **String,** содержа которое содержит имя файла, загружаемого в **поток.** *FileName может* содержать любой допустимый путь и имя в формате UNC. Если указанного файла не существует, возникает ошибка времени запуска.|

## <a name="remarks"></a>Примечания

Этот метод может использоваться для загрузки содержимого локального файла в объект **Stream.** Это может использоваться для отправки содержимого локального файла на сервер.

Объект **Stream** должен быть уже открыт перед вызовом **LoadFromFile.** Этот метод не меняет привязку объекта **Stream;** он по-прежнему будет привязан к объекту, указанному  URL-адресом или **записью,** с которой изначально был открыт поток.

**LoadFromFile** перезаписывает текущее содержимое объекта **Stream** с данными, считаными из файла. Все существующие bytes в **Потоке** перезаписываются содержимым файла. Все ранее существующие и оставшиеся bytes после [EOS,](eos-property-ado.md) созданные **LoadFromFile**, усечены.

После вызова **в LoadFromFile** текущая позиция устанавливается к  началу потока [(позиция](position-property-ado.md) 0).

Поскольку для кодизания в начале потока может быть добавлено 2 бита, размер потока может не совпадать с размером файла, из которого он был загружен.

