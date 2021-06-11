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
ms.openlocfilehash: 394537a60f4cb9603024115ccea67570291d8ac6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419305"
---
# <a name="linking-to-the-mapi-dlls"></a>Связывание с библиотеками DLL MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиенты MAPI могут связаться с DLLs MAPI неявно или явно с помощью функций **Windows LoadLibrary** и **GetProcAddress.** Сведения о явной привязке DLLs MAPI см. в ссылке [на функции MAPI.](how-to-link-to-mapi-functions.md)
  
MAPI предоставляет утверждения определения типов в MAPIX. Файл H-загона для каждой из следующих функций:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Используйте эти определения типа, чтобы правильно вызывать соответствующие точки входа, если вы явно ссылались на DLLs MAPI.
  
Поставщики услуг могут содержать функции, не относящиеся к MAPI, — функции, совершенно не связанные с MAPI, в их DLL. Если необходимо использовать эти функции, прежде чем использовать DLL и **FreeLibrary,** позвоните **в LoadLibrary,** чтобы удалить DLL из памяти после его использования. Так как MAPI не знает о том, что поставщик услуг DLL не использует не MAPI, нет никакой гарантии, что DLL будет доступен при необходимости. MAPI выпускает DLL поставщика услуг, когда больше нет клиентов с активными сеансами, которые требуют его служб. 
  

