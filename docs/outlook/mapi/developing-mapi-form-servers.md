---
title: Разработка серверов форм MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420768"
---
# <a name="developing-mapi-form-servers"></a>Разработка серверов форм MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе описывается процесс создания файлов конфигурации форм-сервера и конфигурации форм для создания настраиваемых форм MAPI. Перед чтением этого раздела необходимо ознакомиться с информацией в [mapi Forms.](mapi-forms.md)
  
Разработка сервера форм включает в себя следующие действия:
  
1. Определение сведений, содержащихся в форме, и выбор набора свойств для удержания этих сведений. Дополнительные сведения см. в подборе набора [свойств формы.](choosing-a-form-s-property-set.md)
    
2. Разработка пользовательского интерфейса, с помощью которого пользователи могут взаимодействовать со свойствами формы.
    
3. Выбор класса сообщений и создание уникального идентификатора класса (CLSID). Обзор классов сообщений см. в [примере MAPI Message Classes.](mapi-message-classes.md) Дополнительные сведения о классах и формах сообщений см. в [подборе класса сообщений.](choosing-a-message-class.md)
    
4. Реализация необходимых интерфейсов форм MAPI, а также любых необязательных интерфейсов, необходимых вашему определенному серверу форм. Дополнительные сведения см. в [статьи Writing Form Server Code](writing-form-server-code.md). 
    
5. Написание кода пользовательского интерфейса для обработки взаимодействия пользователя с объектом формы и свойствами, которые использует форма.
    
6. Создание файла конфигурации формы для формы. Дополнительные сведения см. в [файловом формате файлов конфигурации форм.](file-format-of-form-configuration-files.md)
    
7. Установка формы на компьютерах пользователей. Дополнительные сведения см. [в дополнительных сведениях об](installing-a-form-into-a-library.md)установке формы в библиотеку.
    
Скорее всего, вы будете выполнять шаги от 1 до 5 одновременно, а не завершать их последовательно. Процесс разработки сервера форм, как и многих проектов программирования, не имеет определенной последовательности. Например, создание файла конфигурации формы показано в качестве второго по последнему шагу выше, но вы, вероятно, будете создавать файл конфигурации формы постепенно, и он станет более полным по мере добавления функций на сервер формы.
  
## <a name="see-also"></a>См. также



[Понятия MAPI](mapi-concepts.md)

