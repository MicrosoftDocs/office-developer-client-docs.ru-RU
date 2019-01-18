---
title: Пакетном режиме (Справочник по для настольных баз данных Access)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac5f14d035a4e11cce67f01ca6636f3ebd39963e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717813"
---
# <a name="batch-mode"></a>Пакетный режим

**Применимо к**: Access 2013, Office 2013

Пакетном режиме — в случае свойство **LockType для** задано значение **adLockBatchOptimistic** и обновление пакета поддерживается поставщиком. Некоторые параметры типа блокировки, недоступны в зависимости от расположения курсора. Например тип жесткой блокировки недоступен при **CursorLocation** задано значение **adUseClient**. И наоборот поставщик может не поддерживать оптимистичный блокировки пакета при положения курсора на сервере. Следует использовать пакетного обновления с набором ключей или статических текущей позиции.

Метод **UpdateBatch** используется для отправки **записей** изменения, которые проводятся в буфер копирования на сервер, чтобы обновить источник данных. В следующем разделе мы открытия **набора записей** в пакетном режиме, вносить изменения в буфер копирования и отправьте изменения в источник данных, с помощью вызова **UpdateBatch**.

В этом разделе содержатся следующие разделы:

- [Отправка обновлений: UpdateBatch](sending-the-updates-updatebatch.md)
- [Поиск обновленных записей с помощью фильтра](filtering-for-updated-records.md)
- [Исправление неудачных обновлений](dealing-with-failed-updates.md)
- [Обнаружение и разрешение конфликтов](detecting-and-resolving-conflicts.md)
- [Отключение и повторное подключение набора записей](disconnecting-and-reconnecting-the-recordset.md)
- [Обновление результатов JOINed: уникальная таблица](updating-joined-results-unique-table.md)

