---
title: Использование надежного объекта Application, предоставляемого инструментами разработчика Office для Visual Studio
TOCTitle: Using a trusted application object provided by Office Developer Tools for Visual Studio
ms:assetid: 3778122f-f60e-48e7-8e72-f3aef168bae2
ms:mtpsurl: https://msdn.microsoft.com/library/Bb622502(v=office.15)
ms:contentKeyID: 55119787
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 7b56e59b19f1c9a0ee4c730f14200c3e501f5290
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406115"
---
# <a name="using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio"></a>Использование надежного объекта Application, предоставляемого инструментами разработчика Office для Visual Studio

При разработке управляемой надстройки с помощью инструментов разработчика Office для Visual Studio всегда используйте объект [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)), предоставляемый Visual Studio. 

Если вы не планируете автоматизировать новый экземпляр Outlook, не используйте ключевое слово New или new, чтобы создать новый экземпляр Outlook, поскольку защита объектной модели Outlook не считает этот экземпляр объекта **Application** надежным. 

Если надстройка использует ненадежные экземпляры объекта **Application**, в зависимости от версии Outlook, работающей в клиенте, надстройка по умолчанию будет вызывать защиту объектной модели Outlook для некоторых элементов объектной модели. 

Дополнительные сведения о поведении защиты объектной модели см. в статье [Изменения в Outlook 2007, связанные с безопасностью кода](https://msdn.microsoft.com/library/bb226709\(v=office.15\)). Обратите внимание, что хотя в статье "Изменения в Outlook 2007, связанные с безопасностью кода" надстройки COM считаются надежными по умолчанию, этот дизайн применяется к версиям Outlook, начиная с Outlook 2007, и доверие распространяется на управляемые надстройки аналогичным образом. Независимо от того, является ли надстройка управляемой или нет, доверие основано на предположении, что надстройка использует надежный объект **Application**.

