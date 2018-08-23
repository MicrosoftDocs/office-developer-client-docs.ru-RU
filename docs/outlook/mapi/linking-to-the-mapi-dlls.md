---
title: Связывание с библиотеками DLL MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 428e92dd783368374fa07c8df9629d60e83dd217
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582030"
---
# <a name="linking-to-the-mapi-dlls"></a>Связывание с библиотеками DLL MAPI

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Клиентов MAPI можно связать библиотек MAPI неявно или явно с помощью функции Windows **LoadLibrary** и **GetProcAddress**. Сведения о явно связанные библиотеки MAPI DLL см [ссылка на функции MAPI](how-to-link-to-mapi-functions.md).
  
MAPI предоставляет инструкции определения типа в MAPIX. Файл заголовка для каждого из следующих функций:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Используйте эти определения типов правильно вызов соответствующих точек входа при связывании явно библиотек MAPI.
  
Поставщиков услуг может содержать функции не MAPI — функции, которые полностью не MAPI — в своей библиотеке DLL. Если необходимо использовать следующие компоненты, вызвать **LoadLibrary** перед использованием DLL-Библиотеку и **FreeLibrary** удаление библиотеки DLL из памяти после его использования. Так как MAPI не знает не MAPI варианты использования поставщика услуг DLL-Библиотеку, нет гарантии, что библиотеки DLL будет доступно при необходимости. MAPI освобождает поставщика услуг DLL при больше не все клиенты с активных сеансов, которые требуют его службы. 
  

