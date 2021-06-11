---
title: Тестирование развертывания
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: В этом разделе описаны некоторые сценарии, которые следует проверить на предмет установки и Outlook поставщика социальных соединителя (OSC).
ms.openlocfilehash: 9c811683097a08b9f6e575d4ea2fee29cdd545d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329164"
---
# <a name="testing-deployment"></a>Тестирование развертывания

В этом разделе описаны некоторые сценарии, которые следует проверить на предмет установки и Outlook поставщика социальных соединителя (OSC).

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Наличие Outlook и OSC на клиентских компьютерах

Факторы, влияющие на установку поставщика OSC, включают битность операционной системы, наличие и битность Outlook и включенную в Outlook.
  
Поставщик OSC может быть написан для 32-битной или 64-битной версии OSC. Outlook 2010 и Outlook 2013 доступны в 32-битной и 64-битной версиях, а Office Outlook 2003 и Office Outlook 2007 годов доступны только в 32-битных версиях. В 64-Windows можно установить 32-или 64-Outlook. В 32-битной операционной системе можно установить только 32-битную, но не 64-битную Outlook. В зависимости от битности установленной версии Outlook и поставщика OSC пользователь должен использовать соответствующий установщик для установки поставщика OSC соответствующей битности. Например, если установлен 64-Outlook, а поставщик OSC является родным компонентом com, 32-битный поставщик OSC не будет работать, и пользователь должен использовать соответствующий установщик для установки 64-битного поставщика OSC.
  
Код развертывания поставщика OSC может предполагать, что пользователь имеет поддерживаемую версию Outlook на компьютере. Однако, если текущая версия OSC не находится на клиентском компьютере, код развертывания может скачать и установить соответствующую версию OSC с помощью специально построенных URL-адресов g-link на https://g.live.com . Эти g-ссылки зависят от версии и битности Outlook и локальности клиентского компьютера. Дополнительные сведения об использовании g-links для установки или обновления OSC см. в [контрольном списке установки.](installation-checklist.md)
  
Перед установкой поставщика OSC Outlook должен убедиться, что надстройка OSC включена в Outlook.
  
Рекомендуемый метод развертывания поставщика OSC — использовать пакет Windows (.msi). Проверьте каждый из следующих сценариев, чтобы убедиться, что развертывание работает надлежащим образом для поставщика.
  
|**Сценарий**|**Ожидаемое поведение**|
|:-----|:-----|
|Outlook нет — Outlook 2003 или Outlook 2007 не установлен, а Outlook 2010 или Microsoft Outlook 2013 не установлена и не доставлена в Click-to-Run.  <br/> |Развертывание не удается.  <br/> |
|Outlook 2003 или Outlook 2007 г. не установлен, но Outlook 2010 или Microsoft Outlook 2013 был доставлен click-to-Run.  <br/> |Развернут 32-битный поставщик.  <br/> |
|Outlook 2003 или Outlook 2007 года установлен, но OSC не установлен.  <br/> |Установщик устанавливает OSC и все исправления. После успешной установки OSC установщик развертывает поставщика.  <br/> |
|Outlook 2003 или Outlook 2007 года установлена более ранная версия OSC.  <br/> |Установщик обновляет OSC с помощью g-link для исправлений, а затем развертывает поставщика.  <br/> |
|Outlook 2003 или 2007 годов установлена, а оснащается оснащаться.  <br/> |Установщик развертывает 32-битного поставщика.  <br/> |
|Outlook 2010 или Microsoft Outlook 2013 установлен, но OSC не установлен.  <br/> |Установщик сбой с соответствующим сообщением об ошибке.  <br/> |
|Outlook 2010 или Microsoft Outlook 2013 установлена и установлена более старая версия OSC.  <br/> |Установщик, подходящий для битности установленного Outlook 2010 или Microsoft Outlook 2013, обновляет OSC через g-link для исправлений, а затем развертывает соответствующего поставщика.  <br/> |
|Outlook 2010 или Microsoft Outlook 2013 установлена и оснащается оснащаться.  <br/> |Установщик, подходящий для битности установленного Outlook 2010 или Microsoft Outlook 2013 (32-битного или 64-битного), развертывает соответствующего поставщика.  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Установленные ключи расположения и реестра

Убедитесь в расположении файла, где развернут поставщик OSC, и расположениях в реестре Windows, где создаются ключи реестра для поставщика.
  
### <a name="file-location-for-osc-provider-dlls"></a>Расположение файлов для DLLs поставщика OSC

Проверьте сценарии, указанные в следующей таблице. Обратите внимание, что в таблице перечислены пути установки по умолчанию для DLLs поставщика OSC. Пользователи могут настроить, где они устанавливают эти DLLs.
  
|**Сценарий**|**Ожидаемое поведение**|
|:-----|:-----|
|Microsoft Outlook 2013 устанавливается на клиентский компьютер.  <br/> |DLLs поставщика развернуты в папке Office15. Если операционная система 64-битная и Microsoft Outlook 2013 32-битная, 32-битные DLL развертываются в C:\Program Files (x86)\Microsoft Office\Office15. Если операционная система 64-битная и Microsoft Outlook 2013 64-битная, 64-битные DLL развертываются в C:\Program Files\Microsoft Office\Office15. Если операционная система 32-битная, DLLs развертываются в C:\Program Files\Microsoft Office\Office15.  <br/> |
|Outlook 2010 устанавливается на клиентский компьютер.  <br/> |DLLs поставщика развернуты в папке Office14. Если операционная система 64-битная, а Outlook 2010 — 32-битная, 32-битные DLL развертываются в C:\Program Files (x86)\Microsoft Office\Office14. Если операционная система 64-битная и Outlook 2010 г. — 64-битная, 64-битные DLL развертываются в C:\Program Files\Microsoft Office\Office14. Если операционная система 32-битная, DLLs развертываются в C:\Program Files\Microsoft Office\Office14.  <br/> |
|Outlook 2007 устанавливается на клиентский компьютер.  <br/> |DLLs поставщика развернуты в C:\Program Files\Microsoft Office\Office14. Установка OSC создает папку Office14, и osC должен быть установлен перед любым поставщиком DLLs. См. в предыдущем разделе [Присутствие Outlook и OSC на клиентский компьютер](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Outlook 2003 устанавливается на клиентский компьютер.  <br/> |DLLs поставщика развернуты в C:\Program Files\Microsoft Office\Office14. Установка OSC создает папку Office14, и osC должен быть установлен перед любым поставщиком DLLs. См. в предыдущем разделе [Присутствие Outlook и OSC на клиентский компьютер](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Microsoft Outlook 2013 не установлена, а доставляется с помощью Click-to-Run на клиентский компьютер.  <br/> |DLLs поставщика развернуты в папке Office15. Если операционная система 64-битная, 32-битные DLLs развертываются в C:\Program Files (x86)\Microsoft Office\Office15 или C:\Program Files\Microsoft Office\Office15. Если операционная система 32-битная, DLLs развертываются в C:\Program Files\Microsoft Office\Office15. Если папки Office15 не существует, установка создает папку.  <br/> |
|Outlook 2010 не установлен, а доставлен с помощью click-to-Run на клиентский компьютер.  <br/> |DLLs поставщика развернуты в папке Office14. Если операционная система 64-битная, 32-битные DLLs развертываются в C:\Program Files (x86)\Microsoft Office\Office14 или C:\Program Files\Microsoft Office\Office14. Если операционная система 32-битная, DLLs развертываются в C:\Program Files\Microsoft Office\Office14. Если папки Office14 не существует, установка создает папку.  <br/> |
   
### <a name="windows-registry-locations"></a>Windows реестра

Проверьте следующее:
  
- Установщик поставщика OSC создает значение ProgID для поставщика OSC в Windows реестре либо `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` в `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` . 
    
- Исключением является то, что клиентский компьютер имеет 32-Outlook 64-Windows операционной системе. В этом случае ProgID создается либо `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` в . `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- Ключи реестра должны быть одинаковыми и в том же расположении, если вместо этого DLLs регистрируются regsvr32.exe.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Удаление установки

Ниже приводится несколько тестов, чтобы убедиться, что процесс с целью удалить работает должным образом для поставщика OSC.
  
|**Сценарий**|**Ожидаемое поведение**|
|:-----|:-----|
|Пользователь выбирает, чтобы удалить поставщика.  <br/> |Поставщик uninstalls DLLs и очищает реестр.  <br/> |
|Пользователь выбирает отмену процесса отмены поставщика.  <br/> |Поставщик отменяет процесс отмены и возвращает пользователя в состояние до начала процесса отмены.  <br/> |
   
## <a name="see-also"></a>См. также

- [Регистрация поставщика](registering-a-provider.md)  
- [Контрольный список установки](installation-checklist.md)
- [Получение готовности к выпуску поставщика OSC](getting-ready-to-release-an-osc-provider.md)

