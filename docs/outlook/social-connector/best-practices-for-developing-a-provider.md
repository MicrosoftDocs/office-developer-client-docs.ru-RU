---
title: Рекомендации по разработке поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'При разработке поставщика Outlook Social Connector 2013 (OSC) следует придерживаться следующих правил:'
ms.openlocfilehash: a6ee9d54f33bbc855d178aba844a8f65ec92f964
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812704"
---
# <a name="best-practices-for-developing-a-provider"></a>Рекомендации по разработке поставщика

При разработке поставщика Outlook Social Connector 2013 (OSC) следует придерживаться следующих правил:
  
- По соображениям безопасности поставщиков, которые взаимодействуют с серверами через Интернет следует использовать протокол HTTPS (протокол HTTP (Hypertext Transfer) с помощью Secure сокетов протокол SSL). В противном случае есть риск, адреса электронной почты, действия социальной сети и других пользователей, могут быть перехвачены или предоставляемые в процессе передачи данных.
    
- При создании поставщика OSC для социальных сетей стороннего поставщика, должна придерживаться социальной сети условия использования службы.
    
- Чтобы уменьшить размер пакета загрузки поставщика, построение поставщика с использованием собственного компилятора C++ или других средств, можно создать компонент COM.
    
- В ваш поставщик создайте агент уникальных пользователей, которое отправляется в социальной сети для отслеживания вызовов, сделанных поставщиком для социальных сетей.
    
- Метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) не следует полагаться на вызов социальных сетей в Интернете для получения возможностей поставщика. Например пользователи могут запустить Outlook в автономном режиме; Если OSC вызывает **GetCapabilities** и нет сетевого подключения, **GetCapabilities** вызов не будет возвращен допустимый **возможности** XML. Рекомендуется хранить **возможности** XML в качестве ресурса в поставщике. 
    
- У поставщика OSC можно создать значительного объема звонков в социальных сетях. В зависимости от условия использования службы для социальных сетей рассмотрите возможность кэширования друзья папки Outlook сократить количество вызовов из OSC к поставщику и, в свою очередь, у поставщика в социальной сети.
    
- Office 2013 доступна в 32-разрядной и 64-разрядных версиях. Версии Office до Office 2010, доступны только в 32-разрядная версия. По умолчанию при установке Office 2013 на 64-разрядной ОС Windows — 32-разрядная версия. Если планируется поддерживать 64-разрядная версия OSC, который устанавливается вместе с 64-разрядная версия Office 2013, необходимо также освободить 64-разрядная версия поставщика. 
    
## <a name="see-also"></a>См. также

- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)  
- [Разработка поставщика с использованием схемы XML для OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Развертывание поставщика](deploying-a-provider.md)  
- [Начало разработки поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
