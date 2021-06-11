---
title: Отключение поставщика упакованных магазинов PST
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Последнее изменение: 02 июля 2012 г.'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409946"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Отключение поставщика упакованных магазинов PST

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
После завершения использования поставщика магазина файлов персональных папок (PST) необходимо должным образом закрыть поставщика магазина PST. Дополнительные сведения об использовании поставщика магазина PST, завернутые в пакет, см. в дополнительных сведениях об использовании поставщика магазина [PST.](using-a-wrapped-pst-store-provider.md)
  
Чтобы отключить поставщика магазина PST, необходимо вызвать **[функцию IMSProvider::Shutdown.](imsprovider-shutdown.md)** Эти функции упорядоченно закрывают поставщика магазина PST. 
  
В этом разделе функция **IMSProvider::Shutdown** демонстрируется с помощью примера кода от поставщика магазина магазинов ПСД sample Wrapped. В примере реализован завернутый поставщик PST, который предназначен для использования в сочетании с API репликации. Дополнительные сведения о загрузке и установке поставщика магазинов PST sample wrapped см. в примере Установки поставщика упаковки [PST Store.](installing-the-sample-wrapped-pst-store-provider.md) Дополнительные сведения об API репликации см. в [иллюстрации API репликации.](about-the-replication-api.md)
  
## <a name="shut-down-routine"></a>Отключение рутины

Spooler MAPI вызывает **[функцию IMSProvider::Shutdown](imsprovider-shutdown.md)** непосредственно перед тем, как она выпустит поставщика магазина PST, чтобы поставщик магазина PST, завернутый, может закрыться должным образом. Функция завершает все объекты сеанса, связанные с поставщиком магазина PST. 
  
## <a name="cmsprovidershutdown-example"></a>Пример CMSProvider::ShutDown()

```cpp
STDMETHODIMP CMSProvider::Shutdown(ULONG * pulFlags) 
{ 
    HRESULT hRes = S_OK; 
    Log(true,"CMSProvider::Shutdown\n"); 
    hRes =m_pPSTMS->Shutdown(pulFlags); 
    Log(true,"CMSProvider::Shutdown returned: 0x%08X\n", hRes); 
    return hRes ;  
}
```

## <a name="see-also"></a>См. также



[О поставщике пакетных пакетов PST Store](about-the-sample-wrapped-pst-store-provider.md)
  
[Установка поставщика пакетных пакетов PST](installing-the-sample-wrapped-pst-store-provider.md)
  
[Инициализация поставщика упакованных магазинов PST](initializing-a-wrapped-pst-store-provider.md)
  
[Ведение журнала в поставщике упакованных магазинов PST](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Использование поставщика упакованных магазинов PST](using-a-wrapped-pst-store-provider.md)

