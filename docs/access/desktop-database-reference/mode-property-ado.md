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

Указывает доступные разрешения на изменение данных в [объекте Подключение,](connection-object-ado.md) [Запись](record-object-ado.md)или [Поток.](stream-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает [значение ConnectModeEnum.](connectmodeenum.md) Значение по умолчанию для **подключения** **— adModeUnknown.** Значение по умолчанию для **объекта Record** **— adModeRead.** Значение по умолчанию  для потока, связанного с исходным исходным кодом (открытый с URL-адресом в качестве источника или как поток записи по **умолчанию)** **— adModeRead**.  Значение по умолчанию для **потока,** не связанного с исходным источником (мгновенным в памяти), **— adModeUnknown**.

## <a name="remarks"></a>Примечания

Используйте свойство **Mode** для набора или возврата разрешений доступа, которые используется поставщиком для текущего подключения. Свойство Mode **можно** установить только при закрытии объекта **Подключения.**

Для объекта **Stream,** если режим доступа не указан, он наследуется от источника, используемого для открытия объекта **Stream.** Например, если **поток** открывается из объекта **Record,** по умолчанию он открывается в том же режиме, что и **Запись.**

Это свойство читается или записи, пока объект закрыт и только для чтения, пока объект открыт.

**Удаленное использование службы данных** При этом свойство **Mode** можно задать только **adModeUnknown.**

