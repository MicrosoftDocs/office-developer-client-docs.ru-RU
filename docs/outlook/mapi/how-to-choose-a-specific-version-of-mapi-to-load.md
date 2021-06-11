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

**Область применения**: Outlook 2013 | Outlook 2016 
  
При прямой привязке к реализации MAPI необходимо тщательно выбрать, какую реализацию загрузить. 
  
Существует два способа прямой привязки к реализации MAPI. 
  
1. Вы можете загрузить библиотеку загружки MAPI и указать в реестре настраиваемый DLL для загрузки и отправки звонков MAPI.
    
2. Вы можете реализовать алгоритм поиска клиента MAPI, чтобы найти версию MAPI, используемую клиентом почты по умолчанию, и загрузить его.
    
Поскольку вы можете изменитьMapi32.dll [реестра stub Параметры,](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) чтобы направить приложение на использование любой реализации MAPI, мы рекомендуем направить приложение на использование реализации MAPI, с помощью которую вы протестировали. Ниже описаны оба метода прямой привязки. 
  
## <a name="reading-from-the-registry"></a>Чтение из реестра

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>Чтение сведений о реализации MAPI из реестра

1. Ключи реестра, которые указывают настраиваемый DLL для почтового клиента, находятся под  `HKLM\Software\Clients\Mail` ключом почтового клиента. 
    
   В следующей таблице описаны следующие клавиши:
    
   |**Клавиша**|**Описание**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Идентификатор категории Windows установки PublishComponent (GUID), который определяет DLL, экспортирует простые вызовы MAPI или MAPI. Если установлено, этот ключ имеет приоритет над **ключом DLLPath** или **DLLPathEx.**  <br/> |
   |MSIApplicationLCID  <br/> |Идентификатор locale (LCID) для приложения. Первое строковая величина определяет под ключ от и последующие значения строки определяют значения реестра под этим ключом, которые содержат  `HKLM\Software` сведения о локальном уровне.  <br/> |
   |MSIOfficeLCID  <br/> |LCID для Microsoft Office. Первое строковая величина определяет под ключ от строки и последующие значения строки определяют значения реестра  `HKLM\Software` под этим ключом.  <br/> |
   
   Получение сведений из этих ключей.
    
2. Передай значения, полученные на предыдущем шаге, в функцию [FGetComponentPath.](fgetcomponentpath.md) **FGetComponentPath** — это функция, экспортируемая библиотекой загвоздки MAPI Mapistub.dll. Возвращает путь настраиваемой версии MAPI. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>Загрузка реализации MAPI, помеченной как по умолчанию

1. Прочитайте  `HKLM\Software\Clients\Mail::(default)` значение реестра. 
    
2. Сведения о указанных клиентах, как описано выше.
    
> [!NOTE]
> Обратите внимание, что почтовый клиент по умолчанию может не реализовать расширенный MAPI. 
  
#### <a name="example"></a>Пример

Чтобы загрузить MAPI в соответствии с Outlook, посмотрите на клавиши реестра и передайте их `HKLM\Software\Clients\Mail\Microsoft Outlook` **в FGetComponentPath.** **FGetComponentPath** возвращает путь для Outlook реализации MAPI. 
  
Если ключи **MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID** не заданы, проверьте значение **реестра DLLPathEx.** Если задатки, **FGetComponentPath** дает путь реализации MAPI клиентом. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Реализация алгоритма поиска клиентов MAPI

В следующей таблице перечислены четыре функции MFCMAPI, которые используются для выполнения настраиваемой реализации MAPI:
  
|**Function**|**Описание**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Получает путь библиотеки MAPI.  <br/> |
| `GetMailKey` <br/> |Получает ключ реестра почты MAPI.  <br/> |
| `GetMapiMsiIds` <br/> |Получает идентификатор Windows установки.  <br/> |
| `GetComponentPath` <br/> |Получает путь компонента с [помощью FGetComponentPath.](fgetcomponentpath.md)  <br/> |
   
Так как MFCMAPI загружает по умолчанию реализацию MAPI по умолчанию, если вы хотите использовать другую реализацию MAPI, для этого необходимо явно направить ее. Это выполняется с помощью **процедуры Session\Load MAPI.** 
  
### <a name="how-these-functions-work"></a>Как работают эти функции

1. MFCMAPI  `GetMAPIPath` вызывает, передавая NULL для параметра клиента, для загрузки реализации MAPI по умолчанию.
    
2.  `GetMAPIPath` вызовы для чтения  `GetMapiMsiIds` значений **MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds` вызовы  `GetMailKey` для открытия ключа реестра для почтового клиента по умолчанию. 
    
4.  `GetMapiMsiIds`использует возвращаемую обработку реестра, чтобы найти значения `GetMailKey` **для MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID.**
    
5. Значения для **MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID** возвращаются в  `GetMAPIPath` .  `GetMAPIPath` затем передает их  `GetComponentPath` в .
    
6.  `GetComponentPath` загружает библиотеку замеси MAPI, Mapi32.dll, из каталога системы. 
    
7.  `GetComponentPath` затем извлекает адрес функции **FGetComponentPath** из Mapi32.dll, предполагая, что Mapi32.dll **экспортирует FGetComponentPath**.
    
8. Если получение адреса **FGetComponentPath** из Mapi32.dll не удается, извлекает адрес из  `GetComponentPath` Mapistub.dll. 
    
9.  `GetComponentPath` затем вызывает **FGetComponentPath,** чтобы получить путь по умолчанию версии MAPI.
    
10.  `GetMAPIPath`затем возвращает этот путь вызываемму, который загружает MAPI и явно ссылается на него, как описано в [Link to MAPI Functions.](how-to-link-to-mapi-functions.md)
    
> [!NOTE] 
> - Для поддержки локализованных копий MAPI для английских и не-английских локалов считываю значения для `GetMAPIPath` **подкоев MSIApplicationLCID** и **MSIOfficeLCID.**  `GetMAPIPath` затем вызывает **FGetComponentPath,** сначала указывает **MSIApplicationLCID** как **szQualifier,** и снова указывает **MSIOfficeLCID** как **szQualifier**. Дополнительные сведения о ключах реестра для почтовых клиентов, которые поддерживают не-английские языки, см. в сообщении [Setting Up the MSI Keys for Your MAPI DLL.](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)   
> - Если MFCMAPI не получает путь для использования MAPI, он загружает библиотеку заглов MAPI из  `GetMAPIPath` каталога системы.
> - Значение **реестра MSMapiApps,** о чем говорится в явном сопоставлении звонков MAPI к [DLLs MAPI,](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) применяется только при том, что используется библиотека STUB MAPI. Приложения, загружая определенную реализацию MAPI или загружая реализацию по умолчанию, не должны устанавливать ключ **реестра MSMapiApps.** 
    
## <a name="see-also"></a>См. также

- [FGetComponentPath](fgetcomponentpath.md)
- [Общие сведения о программировании MAPI](mapi-programming-overview.md)
- [Ссылки на функции MAPI](how-to-link-to-mapi-functions.md)
- [Mapi32.dll реестра Stub Параметры](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [Настройка клавиш MSI для DLL MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [Явное сопоставление вызовов MAPI на DLLs MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

