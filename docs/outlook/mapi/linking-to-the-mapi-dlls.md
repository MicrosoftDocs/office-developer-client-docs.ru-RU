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
ms.openlocfilehash: 0bce1d682057b81135d1684c40bc79e6710d4e2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809642"
---
# <a name="linking-to-the-mapi-dlls"></a>Связывание с библиотеками DLL MAPI

  
  
**Относится к**: Outlook 
  
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
  

