---
title: Поддержка поиска для поставщиков хранилищ сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0cd8bbe14e6af020ec5c93cd46a24853d1c8401c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812433"
---
# <a name="supporting-searches-in-message-store-providers"></a>Поддержка поиска для поставщиков хранилищ сообщений

  
  
**Относится к**: Outlook 
  
Клиентские приложения часто имеют некоторые компоненты пользовательского интерфейса посвящен поиск сообщений в хранилище сообщений. Условия поиска в [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) интерфейса с помощью методов [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) и [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) . 
  
Клиенты используют свойство **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) объектов хранилища сообщений для идентификации в корневой папке в хранилище сообщений, содержащая папки для результатов поиска. Папка результатов поиска часто — это папка на верхнем уровне хранилища сообщений, который не является частью дерева папок IPM и следовательно, скрыт.
  
Использует постоянное результатов поиска папок ли поставщика хранилища сообщений или создает один, если это клиент открывает идентификатор записи, хранящиеся в свойстве **PR_FINDER_ENTRYID** это данные реализации. Несколько более поставщика хранилища сообщений для использования в постоянную папку, которая создается при создании хранилища сообщений, так как это так позволяет избежать сложность проверки идентификатор записи при открытии любую папку для просмотра, следует ли создать Папка результатов поиска. Тем не менее не все поставщики хранилища сообщений для этого; Прежде всего хранилища, которые часто предоставляет интерфейс MAPI для прежних версий базы данных или только для чтения сообщения не разрешены или не удается создать папку постоянное результатов поиска в базовый механизм хранения. 
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)
