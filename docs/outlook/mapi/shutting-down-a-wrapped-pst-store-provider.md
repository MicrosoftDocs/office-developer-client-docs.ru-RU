---
title: Завершение работы поставщика упакованного PST-магазина
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409946"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Завершение работы поставщика упакованного PST-магазина

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
После завершения работы с поставщиком упакованного PST-файла необходимо завершить работу поставщика упакованного PST-магазина. Дополнительные сведения об использовании поставщика упакованного PST-магазина см. в сведениях об использовании поставщика упакованного [PST-магазина.](using-a-wrapped-pst-store-provider.md)
  
Чтобы отключить поставщика упакованного PST-магазина, необходимо вызвать функцию **[IMSProvider::Shutdown.](imsprovider-shutdown.md)** Эта функция закрывает поставщика упакованного PST-магазина в упорядоченном порядке. 
  
В этом разделе функция **IMSProvider::Shutdown** демонстрируется с помощью примера кода из примера поставщика упакованного PST-магазина. В примере реализован упакованный поставщик PST,который предназначен для использования в сочетании с API репликации. Дополнительные сведения о загрузке и установке примера поставщика упакованного PST-магазина см. в установке примера поставщика упакованного [PST-магазина.](installing-the-sample-wrapped-pst-store-provider.md) Дополнительные сведения об API репликации см. в сведениях [об API репликации.](about-the-replication-api.md)
  
## <a name="shut-down-routine"></a>Завершение работы программы

Пулер MAPI вызывает функцию **[IMSProvider::Shutdown](imsprovider-shutdown.md)** непосредственно перед выпуском поставщика упакованного PST-магазина, чтобы поставщик упакованного PST-магазина можно было должным образом отключить. Эта функция завершает все объекты сеанса, связанные с поставщиком упакованного PST-хранения. 
  
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



[Пример поставщика упакованного PST-магазина](about-the-sample-wrapped-pst-store-provider.md)
  
[Установка примера поставщика упакованного PST-магазина](installing-the-sample-wrapped-pst-store-provider.md)
  
[Инициализация поставщика упакованного PST-магазина](initializing-a-wrapped-pst-store-provider.md)
  
[Вход в систему поставщика упакованного PST-магазина](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Использование поставщика упакованного PST-магазина](using-a-wrapped-pst-store-provider.md)

