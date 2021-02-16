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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиенты MAPI могут связываться с DLL MAPI неявно или явным образом с помощью функций Windows **LoadLibrary** и **GetProcAddress.** Сведения об явной привязке DLL MAPI см. в ссылке [на функции MAPI.](how-to-link-to-mapi-functions.md)
  
MAPI предоставляет определения типов в MAPIX. Файл h-загона для каждой из следующих функций:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Используйте эти определения типов, чтобы правильно вызывать соответствующие точки входа, если вы явно ссылались на DLL MAPI.
  
Поставщики услуг могут содержать в своей DLL функции, не связанные с MAPI. Если необходимо использовать эти функции, вызовите **LoadLibrary** перед использованием DLL и **FreeLibrary,** чтобы удалить DLL из памяти после ее использования. Поскольку MAPI не знает о том, как DLL поставщика услуг не используется mapI, нет гарантии, что она будет доступна при необходимости. MAPI выпускает DLL поставщика услуг, если больше нет клиентов с активными сеансами, требуя его служб. 
  

