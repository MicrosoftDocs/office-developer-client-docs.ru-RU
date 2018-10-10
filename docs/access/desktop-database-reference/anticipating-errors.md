---
title: Anticipating Errors
TOCTitle: Anticipating Errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f062eb86b45778cc7f25fb2d0d0588b82bdd78b3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482381"
---
# <a name="anticipating-errors"></a>Anticipating Errors


**Применимо к**: Access 2013 | Office 2013

Предотвращение ошибок по крайней мере важно, как обработка ошибок. В этом последнем разделе со списком short меры предосторожности, которые приложение может воспользоваться для ошибки, скорее всего, будет выполнена.

Проверьте состояние объектов, проверив значение свойства **состояние** перед попыткой выполнения операции с помощью этих объектов. Например если приложение использует глобальные **подключения**, проверьте значение свойства **состояние** является ли уже открыт до вызова метода **Open** .

  - Все программы, которые принимает данные от пользователя необходимо включить код для проверки данных перед отправкой в хранилище данных. Нельзя полагаться на хранилище данных, поставщик, ADO или даже язык программирования сообщать о неполадках. Необходимо проверить каждый байт, введенных пользователями, убедившись, что данные правильный ее тип поля и обязательные поля не являются пустыми.

Проверьте данные, прежде чем записи данных в хранилище данных. Для этого проще всего обрабатывать события **WillMove** или **WillUpdateRecordset** события. Более подробные сведения об обработке событий ADO, в разделе [Глава 7: обработка событий ADO](chapter-7-handling-ado-events.md).

Убедитесь в том, что **набора записей** объекты не за пределами **записей** перед попыткой перемещения указателя записи. При попытке **MoveNext** Если **EOF** имеет значение True или **MovePrev** , если **BOF** имеет значение True, произойдет ошибка. При выполнении любой из методов **перемещения** , когда **EOF** и **BOF** имеют значение True, возникнет ошибка.

Также возникают ошибки при попытке выполнения операции, такие как **файлы и **поиска** ** на пустой **набор записей**.
