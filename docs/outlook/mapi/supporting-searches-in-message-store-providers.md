---
title: Поддержка поиска в поставщиках магазинов сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425388"
---
# <a name="supporting-searches-in-message-store-providers"></a>Поддержка поиска в поставщиках магазинов сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения часто имеют некоторые компоненты пользовательского интерфейса, посвященные поиску сообщений в хранилище сообщений. Критерии поиска указаны в [интерфейсе IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) с помощью методов [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) и [IMAPIContainer::GetSearchCriteria.](imapicontainer-getsearchcriteria.md) 
  
Клиенты используют свойство PR_FINDER_ENTRYID объекта хранения **сообщений** [(PidTagFinderEntryId)](pidtagfinderentryid-canonical-property.md)для идентификации корневой папки в хранилище сообщений, содержащем папки для результатов поиска. Папка результатов поиска часто является папкой на верхнем уровне магазина сообщений, которая не входит в дерево папок IPM и поэтому скрыта.
  
Использует ли поставщик магазина сообщений постоянную папку результатов поиска или создает ее при  открываемом клиентом идентификаторе записи, хранящемся в свойстве PR_FINDER_ENTRYID, является деталью реализации. Поставщику магазина сообщений несколько проще использовать постоянную папку, созданную при создании магазина сообщений, так как это позволяет избежать сложности проверки идентификатора записи при открываемой папке, чтобы узнать, следует ли создавать папку результатов поиска. Однако не все поставщики магазинов сообщений могут это сделать; в частности, хранилища или хранилища сообщений только для чтения, которые предоставляют интерфейс MAPI в устаревшую базу данных, часто не допускаются или не могут создать постоянную папку результатов поиска в основном механизме хранения. 
  
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

