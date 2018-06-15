---
title: Выбор определенной версии MAPI для загрузки
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: d0bce7b3a12f259b7ac5f28219c8a92dd2200f07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808590"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Выбор определенной версии MAPI для загрузки

**Применимо к**: Outlook 
  
При связывании явно реализация интерфейса MAPI, необходимо тщательно выбрать реализация для загрузки. 
  
Существует два метода для связывания явно реализация интерфейса MAPI. 
  
1. Можно загрузить библиотеку заглушка MAPI и укажите в вызовы пользовательских DLL для загрузки и отправки MAPI реестра.
    
2. Можно реализовать алгоритм подстановки клиента MAPI для поиска версия MAPI, используемых почтового клиента по умолчанию и загрузить его.
    
Можно изменить [Параметры реестра Mapi32.dll заглушку](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx) для направления приложения для использования любой реализации интерфейса MAPI, поэтому рекомендуется прямое подключение приложения для использования реализация интерфейса MAPI, проверенного с. Ниже описаны оба метода компоновки явным образом. 
  
## <a name="reading-from-the-registry"></a>Чтение из реестра

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>Чтение из реестра сведения о реализации интерфейса MAPI

1. Разделы реестра, которые указывают пользовательской библиотеки DLL для почтового клиента, находятся в разделе `HKLM\Software\Clients\Mail` ключа почтового клиента. 
    
   В следующей таблице описываются эти разделы:
    
   |**Key**|**Описание**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Вызывает PublishComponent установщика Windows категории идентификатор (GUID), идентифицирующий библиотеки DLL, которая экспортирует простой MAPI или MAPI. Если набор, этот раздел приоритет над **DLLPath** или **DLLPathEx** ключа.  <br/> |
   |MSIApplicationLCID  <br/> |Код языка (LCID) для вашего приложения. Первая строка значение определяет подраздел из `HKLM\Software` и последующих строковые значения идентификации пример значения реестра, которые содержат сведения о языковом стандарте.  <br/> |
   |MSIOfficeLCID  <br/> |Коды языка для Microsoft Office. Первая строка значение определяет подраздел из `HKLM\Software` и последующих строковые значения определение значения реестра под этот ключ.  <br/> |
   
   Получите данные из этих разделов.
    
2. Передайте значения, которые вы получили из предыдущего шага в функцию [FGetComponentPath](fgetcomponentpath.md) . **FGetComponentPath** — это функция, который экспортируется в библиотеке заглушка MAPI Mapistub.dll. Она возвращает путь настраиваемой версии MAPI. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>Чтобы загрузить реализации интерфейса MAPI, помеченные как по умолчанию

1. Чтение `HKLM\Software\Clients\Mail::(default)` значения реестра. 
    
2. Поиск сведений для указанного клиента, как описано выше.
    
> [!NOTE]
> Обратите внимание на то, что почтового клиента по умолчанию не может внедрить расширенного MAPI. 
  
#### <a name="example"></a>Пример

Чтобы загрузить MAPI, реализованные в Outlook, поиск разделов реестра в разделе `HKLM\Software\Clients\Mail\Microsoft Outlook` и передавайте их **FGetComponentPath**. **FGetComponentPath** возвращает путь для реализации Outlook MAPI. 
  
Если ключи **MSIComponentID**, **MSIApplicationLCID**и **MSIOfficeLCID** не задано, проверьте значение реестра **DLLPathEx** . Если заданы ключи, **FGetComponentPath** дает пути реализации клиента MAPI. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Реализация алгоритма поиска клиентов MAPI

В следующей таблице приведены четыре функций из mfcmapi (en), которые используются для поиска путь для настраиваемая реализация интерфейса MAPI:
  
|**Функция**|**Описание**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Возвращает путь к библиотеке MAPI.  <br/> |
| `GetMailKey` <br/> |Получает раздел реестра почты MAPI.  <br/> |
| `GetMapiMsiIds` <br/> |Получает идентификатор установщика Windows.  <br/> |
| `GetComponentPath` <br/> |Возвращает путь к компоненту, с помощью [FGetComponentPath](fgetcomponentpath.md).  <br/> |
   
Так как mfcmapi (en) загружается по умолчанию реализация интерфейса MAPI по умолчанию, если вы хотите использовать другой реализации интерфейса MAPI, необходимо явно прямой соответствующим образом. Это выполняется с помощью процедуры **Session\Load MAPI** . 
  
### <a name="how-these-functions-work"></a>Как работают эти функции

1. Mfcmapi (en) вызовы `GetMAPIPath`, передача NULL для параметра клиента для загрузки реализация интерфейса MAPI по умолчанию.
    
2.  `GetMAPIPath`вызовы `GetMapiMsiIds` считывать значения для **MSIComponentID**, **MSIApplicationLCID**и **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds`вызовы `GetMailKey` открыть раздел реестра для почтового клиента по умолчанию. 
    
4.  `GetMapiMsiIds`с помощью реестра дескриптор, возвращенный `GetMailKey` для поиска значений для **MSIComponentID**, **MSIApplicationLCID**и **MSIOfficeLCID**.
    
5. Возвращаемые значения для **MSIComponentID**, **MSIApplicationLCID**и **MSIOfficeLCID**, чтобы `GetMAPIPath`.  `GetMAPIPath`передает их `GetComponentPath`.
    
6.  `GetComponentPath`загружает библиотеку заглушка MAPI, Mapi32.dll, из каталога системы. 
    
7.  `GetComponentPath`затем извлекает адрес функции **FGetComponentPath** из Mapi32.dll, при условии, что Mapi32.dll экспортирует **FGetComponentPath**.
    
8. Если получение адреса **FGetComponentPath** из возникает ошибка Mapi32.dll `GetComponentPath` извлекает адрес из Mapistub.dll. 
    
9.  `GetComponentPath`затем вызывает **FGetComponentPath**, получение путь по умолчанию версии MAPI.
    
10.  `GetMAPIPath`затем возвращает этот путь к вызывающему, который затем загружает MAPI и явно приведены ссылки на него, как описано в [ссылка на функции MAPI](how-to-link-to-mapi-functions.md).
    
> [!NOTE] 
> - Для поддержки локализованных копий MAPI для английского языка и языковых стандартов неанглийской `GetMAPIPath` считывает значения для **MSIApplicationLCID** и **MSIOfficeLCID** подразделы.  `GetMAPIPath`затем вызывает **FGetComponentPath**, сначала указав **MSIApplicationLCID** как **szQualifier**, а еще раз **MSIOfficeLCID** как **szQualifier**. Дополнительные сведения о разделах реестра для почтовых клиентов, которые поддерживают языками см [параметр копирование MSI для Your MAPI DLL](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx).   
> - Если mfcmapi (en) не получает путь для использования интерфейса MAPI `GetMAPIPath`, он загружает библиотеку заглушка MAPI из каталога системы.
> - Параметр реестра **MSMapiApps** , обсуждаемые в [Явно сопоставление вызовов программного интерфейса MAPI для библиотеки MAPI DLL](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx) применяется только при использовании библиотеки заглушка MAPI. Приложения, которые загрузить реализации интерфейса MAPI или загрузить реализация по умолчанию не нужно задать раздел реестра **MSMapiApps** . 
    
## <a name="see-also"></a>См. также

- [FGetComponentPath](fgetcomponentpath.md)
- [����� �������� � ���������������� MAPI](mapi-programming-overview.md)
- [Ссылка на функции MAPI](how-to-link-to-mapi-functions.md)
- [Параметры реестра заглушка Mapi32.dll](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx)
- [Настройка разделов MSI для библиотеки DLL MAPI](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx)
- [Явным образом сопоставление вызовов программного интерфейса MAPI для библиотеки MAPI DLL](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx)

