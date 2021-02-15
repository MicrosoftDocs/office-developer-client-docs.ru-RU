---
title: Свойство Mode (ADO)
TOCTitle: Mode property (ADO)
ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15)
ms:contentKeyID: 48545227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f30dac303541b0f53d06eb7756739ff1add6ce0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288871"
---
# <a name="mode-property-ado"></a>Свойство Mode (ADO)


**Область применения**: Access 2013, Office 2013

Указывает доступные разрешения на изменение данных в [объекте Connection,](connection-object-ado.md) [Record](record-object-ado.md)или [Stream.](stream-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [ConnectModeEnum.](connectmodeenum.md) Значением по умолчанию для **подключения** **является adModeUnknown.** Значение по умолчанию для **объекта Record** **— adModeRead.** Значением по  умолчанию для потока, связанного с исходным источником (открываемым  с URL-адресом в качестве источника или в качестве потока записи по **умолчанию)** является **adModeRead.** Значением по умолчанию для **потока, не** связанного с исходным источником (который был задан в памяти) **является adModeUnknown.**

## <a name="remarks"></a>Заметки

Используйте свойство **Mode,** чтобы установить или вернуть разрешения доступа, которые использует поставщик для текущего подключения. Свойство Mode **можно** установить только при закрытии объекта **Connection.**

Для объекта **Stream,** если режим доступа не указан, он наследуется от источника, используемого для открытия объекта **Stream.** Например, если **поток** открывается из объекта **Record,** по умолчанию он открывается в том же режиме, что и **запись.**

Это свойство считывать и записывать, когда объект закрывается и только для чтения, когда объект открыт.

**Использование удаленной службы данных** При использования в клиентском объекте Connection свойство **Mode** можно установить только в **adModeUnknown.**

