---
title: 'Chapter 5: Updating and Persisting Data'
TOCTitle: 'Chapter 5: Updating and Persisting Data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 91c747c970988a9ca853f0be66f5c0b485f5c3f6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480063"
---
# <a name="chapter-5-updating-and-persisting-data"></a>Chapter 5: Updating and Persisting Data


**Применимо к**: Access 2013 | Office 2013

Предыдущая главы рассматриваются способы использования ADO для получения данных в источнике данных, как просматривать данные и даже как для изменения данных. Конечно Если целью приложения является разрешить пользователям изменять данные, необходимо понять, как сохранить изменения. Либо можно сохранять изменения **записей** в файл с помощью метода **Сохранить** или отправке изменений обратно в источник данных для хранения данных с помощью метода **Update** или **UpdateBatch** .

В предыдущем главы изменены данные в нескольких строках **набора записей**. ADO поддерживает две основные понятия, связанные с Добавление, удаление и изменение строк данных.

— Это первый общее представление о том, что не внесены изменения сразу же **набора записей**; Вместо этого они выполняются внутреннего *буфера копирования*. Если вы решили, что изменения не нужно, изменения в буфере копии будут удалены. Если необходимо сохранить изменения, изменения в буфер копирования применяются к **набора записей**.

Общее представление о второй — это изменения, либо распространить на источник данных, сразу же работы, объявляемые в строке полный (то есть, режим *интерпретации* ) или сбора все изменения в набор строк, пока не объявить рабочего набора завершения (это *пакетном* режиме). Свойство **LockType для** определяет при внесении изменений в источнике данных. **adLockOptimistic** или **adLockPessimistic** режим интерпретации, а **adLockBatchOptimistic** указывает пакетном режиме. Свойство **CursorLocation** влияет на доступные параметры **LockType для** . Например параметр **adLockPessimistic** не поддерживается, если свойство **CursorLocation** имеет значение **adUseClient**.

В режиме интерпретации каждого вызова метода **Update** распространяет изменения к источнику данных. В пакетном режиме каждого вызова **обновления** или перемещения из текущей позиции строки сохраняет изменения в буфер копирования, но только метод **UpdateBatch** распространяет изменения к источнику данных.
