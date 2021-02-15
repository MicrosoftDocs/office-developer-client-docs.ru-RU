---
title: Batch mode (Access desktop database reference)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac5f14d035a4e11cce67f01ca6636f3ebd39963e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296880"
---
# <a name="batch-mode"></a>Пакетный режим

**Область применения**: Access 2013, Office 2013

Пакетный режим действует, когда свойству **LockType** задают свойство **adLockBatchOptimistic,** а пакетное обновление поддерживается поставщиком. Некоторые параметры типа блокировки недоступны в зависимости от расположения курсора. Например, пессимистичный тип блокировки не доступен, если для **cursorLocation** установлено в **adUseClient.** И наоборот, поставщик может не поддерживать пакетную оптимистичную блокировку, если курсор расположен на сервере. Пакетное обновление следует использовать только с набором клавиш или статическим курсором.

Метод **UpdateBatch** используется для отправки изменений **recordset,** которые удерживаются в буфере копирования, на сервер для обновления источника данных. В следующем разделе мы откроем набор записей в пакетном режиме, внесем изменения в буфер копирования, а затем отправим изменения в источник данных с помощью вызова **UpdateBatch.** 

В этой статье содержатся следующие разделы:

- [Отправка обновлений: UpdateBatch](sending-the-updates-updatebatch.md)
- [Поиск обновленных записей с помощью фильтра](filtering-for-updated-records.md)
- [Исправление неудачных обновлений](dealing-with-failed-updates.md)
- [Обнаружение и разрешение конфликтов](detecting-and-resolving-conflicts.md)
- [Отключение и повторное подключение набора записей](disconnecting-and-reconnecting-the-recordset.md)
- [Обновление результатов JOINed: уникальная таблица](updating-joined-results-unique-table.md)

