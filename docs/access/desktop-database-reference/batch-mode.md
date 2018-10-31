---
title: Пакетном режиме (Справочник по для настольных баз данных Access)
TOCTitle: Batch Mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37f66f6ef6c4ed63b106584a6ac5118cddf20526
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861205"
---
# <a name="batch-mode"></a>Пакетный режим


**Применимо к**: Access 2013 | Office 2013

Пакетном режиме — в случае свойство **LockType для** задано значение **adLockBatchOptimistic** и обновление пакета поддерживается поставщиком. Некоторые параметры типа блокировки, недоступны в зависимости от расположения курсора. Например тип жесткой блокировки недоступен при **CursorLocation** задано значение **adUseClient**. И наоборот поставщик может не поддерживать оптимистичный блокировки пакета при положения курсора на сервере. Следует использовать пакетного обновления с набором ключей или статических текущей позиции.

Метод **UpdateBatch** используется для отправки **записей** изменения, которые проводятся в буфер копирования на сервер, чтобы обновить источник данных. В следующем разделе мы открытия **набора записей** в пакетном режиме, вносить изменения в буфер копирования и отправьте изменения в источник данных, с помощью вызова **UpdateBatch**.

В этом разделе содержатся следующие разделы:

- [Отправка обновлений: UpdateBatch](sending-the-updates-updatebatch.md)

- [Фильтрация для обновленных записей](filtering-for-updated-records.md)

- [Исправление неудачных обновлений](dealing-with-failed-updates.md)

- [Обнаружение и разрешение конфликтов](detecting-and-resolving-conflicts.md)

- [Отключение и повторное подключение набора записей](disconnecting-and-reconnecting-the-recordset.md)

- [Обновление результатов JOINed: уникальная таблица](updating-joined-results-unique-table.md)

