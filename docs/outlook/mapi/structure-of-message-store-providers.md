---
title: Структура поставщиков хранилищ сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: eda62a4cd31e0de695d52391a6717e7a0f5ea581
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426424"
---
# <a name="structure-of-message-store-providers"></a>Структура поставщиков хранилищ сообщений
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поставщик хранения сообщений при работе в памяти — это [интерфейс IMSProvider: IUnknown.](imsprovideriunknown.md) Интерфейс **IMSProvider** позволяет клиентские приложения и шпалер MAPI войти в хранилище сообщений и выйти из него. Интерфейсы, которые клиентские приложения и шпалер MAPI используют для доступа к папкам и сообщениям в хранилище сообщений, это [интерфейсы IMSLogon](imslogoniunknown.md) и [IMsgStore.](imsgstoreimapiprop.md) Эти интерфейсы обычно создаются при первом входе в хранилище сообщений, хотя точка входа [MSProviderInit](msproviderinit.md) В хранилище сообщений DLL также может создавать их. 
  
Так как **интерфейсы IMSLogon** и **IMsgStore** имеют несколько методов, может быть проще создать объект класса, унаследованный от обоих этих интерфейсов. Вы также можете реализовать эти интерфейсы в отдельных объектах и написать внутренние функции помощника в DLL, которые реализуют общие методы, которые затем можно назвать из методов в **интерфейсах IMSLogon** и **IMsgStore.** 
  
На следующем рисунке показан план иерархии объектов высокого уровня в хранилище запущенных сообщений.
  
**Иерархия объектов хранилища сообщений**
  
![Иерархия объектов хранения сообщений.](media/storeobj.gif "Иерархия объектов хранения сообщений")
  
## <a name="see-also"></a>См. также

- [Разработка поставщика хранилища сообщений MAPI](developing-a-mapi-message-store-provider.md)

