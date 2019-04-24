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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270044"
---
# <a name="linking-to-the-mapi-dlls"></a>Связывание с библиотеками DLL MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиенты MAPI могут связываться с библиотеками MAPI неявным образом или явным образом с помощью функций Windows, **LoadLibrary** и **GetProcAddress**. Сведения о явном связывании библиотек DLL MAPI приведены [в статье ссылки на функции MAPI](how-to-link-to-mapi-functions.md).
  
MAPI предоставляет операторы определения типов в МАПИКС. H файл заголовков для каждой из следующих функций:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Используйте эти определения типов, чтобы правильно вызывать соответствующие точки входа, если вы явно связываетесь с библиотеками MAPI.
  
Поставщики услуг могут содержать функции, не связанные с MAPI, — функции, полностью несвязанные с MAPI, в их DLL-БИБЛИОТЕКАх. Если вам нужно использовать эти функции, вызовите **LoadLibrary** перед использованием DLL и **FreeLibrary** , чтобы удалить библиотеку DLL из памяти после ее использования. Так как MAPI не знает об использовании библиотеки DLL поставщика услуг, отличной от MAPI, не гарантируется, что библиотека DLL будет доступна при необходимости. MAPI освобождает БИБЛИОТЕКУ DLL поставщика услуг, когда больше нет клиентов с активными сеансами, для которых требуются службы. 
  

