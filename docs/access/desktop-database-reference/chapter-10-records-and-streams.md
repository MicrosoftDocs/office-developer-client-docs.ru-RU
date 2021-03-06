---
title: Глава 10. Записи и потоки
TOCTitle: 'Chapter 10: Records and streams'
ms:assetid: 74862096-2273-3b61-f89c-06554ccf42cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249477(v=office.15)
ms:contentKeyID: 48545663
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a47ac1f850905546651ffbdd708887bf7d74940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296495"
---
# <a name="chapter-10-records-and-streams"></a>Глава 10. Записи и потоки

**Область применения**: Access 2013, Office 2013

ADO в настоящее время предоставляет объект[Recordset](recordset-object-ado.md) в качестве основного средства доступа к информации в источниках данных, таких как реляционные базы данных. Однако некоторые поставщики поддерживают объекты [Record](record-object-ado.md) и [Stream](stream-object-ado.md) в качестве альтернативных или взаимодополняющих объектов, с которыми можно манипулировать данными от поставщиков. Подробнее о поведении **записи** см. в документации поставщика.

## <a name="records"></a>Записи

**Записывая** объекты, по сути, функционируют как однорядные **recordset** s. Однако **записи имеют** ограниченные функциональные возможности по сравнению с **recordsets** и имеют различные свойства и методы. Источником данных в объекте **Record** может быть команда, которая возвращает один ряд данных от поставщика. Использование **объектов Record,** а не **объектов Recordset** для получения результатов из запроса, возвращающего один ряд данных, устраняет накладную часть моментации более сложного объекта **Recordset.**

**Объекты** записи могут служить другой цели, особенно с поставщиками источников данных, помимо традиционных реляционных баз данных, таких как Поставщик DB Microsoft OLE для [публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md) Большая часть информации, которую необходимо обрабатывать, существует не в виде таблиц в базах данных, а в виде сообщений в системах электронной почты и файлах в современных файловой системе. Объекты **Record** и **Stream** облегчают доступ к сведениям, хранимым в источниках, помимо реляционных баз данных.

Объект **Record** может представлять и управлять данными, такими как каталоги и файлы в файловой системе или папках и сообщениях в системе электронной почты. Для этих целей источником  записи может быть текущая строка open **Recordset,** абсолютный URL-адрес или относительный URL-адрес в сочетании с объектом open [Connection.](connection-object-ado.md)

Как правило, **набор Recordset можно** использовать для представления контейнера или родителя в иерархии, например папки или каталога. Запись **может** использоваться для возврата определенных сведений об одном узле родительского контейнера, например файле или документе. Основная **причина, по** которой записи используются для представления данных этого типа, заключается в том, что эти источники данных являются разнородными. Это означает, что **у каждой записи** может быть свой набор и количество полей. Традиционные **записи,** содержащие строки из базы данных, однородны, что означает, что каждая строка имеет одинаковое число и тип полей.

Дополнительные сведения об использовании объекта **Record** для обработки этих разнородных данных от поставщиков, таких как поставщик публикаций в Интернете, см. в публикации ["Использование ADO для интернет-публикации".](using-ado-for-internet-publishing.md)

## <a name="streams"></a>Потоки

Объект **Stream** предоставляет средства для чтения, записи и управления потоком bytes. Этот поток byte может быть текстовым или двоичным и ограничен размером только системных ресурсов. Как правило, объекты ADO **Stream** используются для следующих целей:

- Чтобы содержать текст или bytes, которые составляют файл или сообщение, обычно используется с поставщиками, такими как Поставщик DB Microsoft OLE для интернет-публикации. Дополнительные сведения об использовании объектов **Stream** см. в публикации ["Использование ADO для интернет-публикации".](using-ado-for-internet-publishing.md)

Объект **Stream** можно открыть по:

- Простой файл, указанный с URL-адресом.

- Поле Record **или** **Recordset, содержащее** **объект Stream.**

- Поток объекта Record **или** **Recordset** по умолчанию, представляющего каталог или сложный файл.

- Поле ресурсов, содержащее URL-адрес простого файла.

- Нет конкретного источника вообще. В этом случае объект **Stream** открывается в памяти. Данные можно написать в него, а затем сохранить в другом **потоке** или файле.

- BLOB-поле в **наборе записей.**

В этой главе освещают следующие темы:

- [Потоки и сохраняемость](streams-and-persistence.md)
- [Записи и поля от поставщика](records-and-provider-supplied-fields.md)
- [Абсолютные и относительные URL-адреса](absolute-and-relative-urls.md)
- [Использование ADO для публикации в Интернете (ADO)](using-ado-for-internet-publishing.md)
