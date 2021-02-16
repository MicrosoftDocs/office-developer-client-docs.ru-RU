---
title: Выбор определенной версии MAPI для загрузки
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344522"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Выбор определенной версии MAPI для загрузки

**Относится к**: Outlook 2013 | Outlook 2016 
  
При явной привязке к реализации MAPI необходимо тщательно выбирать загружаемую реализацию. 
  
Существует два способа явной привязки к реализации MAPI. 
  
1. Вы можете загрузить библиотеку загружок MAPI и указать в реестре настраиваемую библиотеку DLL для загрузки и отправки вызовов MAPI.
    
2. Вы можете реализовать алгоритм поиска клиента MAPI, чтобы найти версию MAPI, используемую почтовым клиентом по умолчанию, и загрузить его.
    
Так как вы можете [ изменить](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)Mapi32.dll реестра, чтобы приложение было использовать любую реализацию MAPI, рекомендуется направлять приложение на использование проверенной вами реализации MAPI. Ниже описаны оба способа явного связывания. 
  
## <a name="reading-from-the-registry"></a>Чтение из реестра

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>Чтение сведений о реализации MAPI из реестра

1. Ключи реестра, которые указывают настраиваемую DLL для почтового клиента, расположены под  `HKLM\Software\Clients\Mail` ключом почтового клиента. 
    
   В следующей таблице описаны следующие ключи:
    
   |**Клавиша**|**Описание**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Идентификатор категории (GUID) установщика Windows, который определяет DLL,который экспортирует простые вызовы MAPI или MAPI. Если этот ключ задается, он имеет приоритет над **ключом DLLPath** или **DLLPathEx.**  <br/> |
   |MSIApplicationLCID  <br/> |Код локального идентификатора (LCID) для приложения. Первое строковая строка определяет под ключ из, а последующие строки определяют значения реестра под этим ключом, содержащие сведения  `HKLM\Software` о региональных значениях.  <br/> |
   |MSIOfficeLCID  <br/> |LCID для Microsoft Office. Первое строка определяет под ключ, а последующие строки определяют значения реестра  `HKLM\Software` под этим ключом.  <br/> |
   
   Получите информацию из этих ключей.
    
2. Передав значения, полученные на предыдущем шаге, в функцию [FGetComponentPath.](fgetcomponentpath.md) **FGetComponentPath** — это функция, экспортируемая библиотекой заг Mapistub.dll. Он возвращает путь к пользовательской версии MAPI. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>Загрузка реализации MAPI, отмеченной как стандартная

1. Прочитайте  `HKLM\Software\Clients\Mail::(default)` значение реестра. 
    
2. Найди сведения для указанных клиентов, как описано выше.
    
> [!NOTE]
> Обратите внимание, что почтовый клиент по умолчанию может не реализовать расширенный MAPI. 
  
#### <a name="example"></a>Пример

Чтобы загрузить MAPI, реализованные в Outlook, найди под ними ключи реестра и передайте их `HKLM\Software\Clients\Mail\Microsoft Outlook` **в FGetComponentPath.** **FGetComponentPath** вернет путь для реализации MAPI в Outlook. 
  
Если ключи **MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID** не заданы, проверьте значение **реестра DLLPathEx.** Если ключи за установлены, **FGetComponentPath** предоставляет путь реализации MAPI клиента. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Реализация алгоритма поиска клиента MAPI

В следующей таблице перечислены четыре функции из MFCMAPI, которые используются для искомого пути для пользовательской реализации MAPI:
  
|**Function**|**Описание**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Получает путь к библиотеке MAPI.  <br/> |
| `GetMailKey` <br/> |Получает ключ реестра почты MAPI.  <br/> |
| `GetMapiMsiIds` <br/> |Получает идентификатор установщика Windows.  <br/> |
| `GetComponentPath` <br/> |Получает путь к компоненту с помощью [FGetComponentPath.](fgetcomponentpath.md)  <br/> |
   
Так как MFCMAPI загружает стандартную реализацию MAPI по умолчанию, если вы хотите использовать другую реализацию MAPI, для этого необходимо явным образом направить ее. Это выполняется с помощью **процедуры Session\Load MAPI.** 
  
### <a name="how-these-functions-work"></a>Как работают эти функции

1. Вызовы MFCMAPI  `GetMAPIPath` с передачей NULL для параметра клиента для загрузки реализации MAPI по умолчанию.
    
2.  `GetMAPIPath`вызовы для чтения значений `GetMapiMsiIds` **MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID.**
    
3.  `GetMapiMsiIds``GetMailKey`вызовы, чтобы открыть ключ реестра для почтового клиента по умолчанию. 
    
4.  `GetMapiMsiIds`использует работку реестра, возвращаемую для возвращения значений `GetMailKey` **для MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID.**
    
5. Значения **MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID** возвращаются в  `GetMAPIPath` .  `GetMAPIPath` затем передает их в  `GetComponentPath` .
    
6.  `GetComponentPath` загружает библиотеку загона MAPI Mapi32.dll из системного каталога. 
    
7.  `GetComponentPath`затем извлекает адрес функции **FGetComponentPath** из Mapi32.dll при условии, что Mapi32.dll **экспортирует FGetComponentPath.**
    
8. Если получить адрес **FGetComponentPath** из Mapi32.dll не удается, получает адрес из  `GetComponentPath` Mapistub.dll. 
    
9.  `GetComponentPath` Затем **вызывается FGetComponentPath,** который получает путь к версии MAPI по умолчанию.
    
10.  `GetMAPIPath`затем возвращает этот путь вызываемой, которая затем загружает MAPI и явным образом ссылается на него, как описано в ссылке на [функции MAPI.](how-to-link-to-mapi-functions.md)
    
> [!NOTE] 
> - Для поддержки локализованных копий MAPI для английского и неименизованного языка считывайте значения подкайки `GetMAPIPath` **MSIApplicationLCID** и **MSIOfficeLCID.**  `GetMAPIPath`затем вызывает **FGetComponentPath,** сначала укажите **MSIApplicationLCID** как **szQualifier,** а затем снова укажите **MSIOfficeLCID** как **szQualifier.** Дополнительные сведения о ключах реестра для почтовых клиентов, которые поддерживают не английский язык, см. в настройке [ключей MSI для вашей DLL MAPI.](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)   
> - Если MFCMAPI не получает путь для использования MAPI, он загружает библиотеку загружки  `GetMAPIPath` MAPI из системного каталога.
> - Значение **реестра MSMapiApps,** обсуждаемые в явном сопоставлении вызовов MAPI с [библиотеками DLL MAPI,](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) применяется только в том случае, если используется библиотека ЗАГТ MAPI. Приложения, которые загружают определенную реализацию MAPI или загружают реализацию по умолчанию, не должны устанавливать **ключ реестра MSMapiApps.** 
    
## <a name="see-also"></a>См. также

- [FGetComponentPath](fgetcomponentpath.md)
- [Общие сведения о программировании MAPI](mapi-programming-overview.md)
- [Ссылки на функции MAPI](how-to-link-to-mapi-functions.md)
- [Mapi32.dll реестра загной](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [Настройка ключей MSI для DLL MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [Явное сопоставление вызовов MAPI с DLL MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

