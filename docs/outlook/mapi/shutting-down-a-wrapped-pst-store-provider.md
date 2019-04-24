---
title: Завершение работы поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Дата последнего изменения: 02 июля 2012 г.'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282784"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Завершение работы поставщика упакованного PST-хранилища

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
После завершения работы с упакованным поставщиком хранилища PST-файлов в оболочке необходимо надлежащим образом отключить поставщика упакованного PST-хранилища. Более подробную информацию об использовании поставщика упакованного PST-хранилища можно узнать в статье [Использование поставщика упакованНОГО PST-хранилища](using-a-wrapped-pst-store-provider.md).
  
Для завершения работы поставщика упакованного PST-хранилища необходимо вызвать функцию **[функцииimsprovider:: Shutdown](imsprovider-shutdown.md)** . Эта функция закрывает поставщика упакованного PST-хранилища в нужном порядке. 
  
В этой статье функция **функцииimsprovider:: Shutdown** показана с помощью примера кода из примера поставщика УПАКОВАНного PST-хранилища. В примере реализуется упакованный поставщик PST, предназначенный для использования вместе с API репликации. Дополнительные сведения о загрузке и установке примера поставщика упакованного PST-хранилища можно найти в статье [Установка примера поставщика упакованНОГО PST-хранилища](installing-the-sample-wrapped-pst-store-provider.md). Более подробную информацию об API репликации можно узнать [в статье о API репликации](about-the-replication-api.md).
  
## <a name="shut-down-routine"></a>Подпрограмма завершения работы

Диспетчер очереди MAPI вызывает функцию **[функцииimsprovider:: Shutdown](imsprovider-shutdown.md)** непосредственно перед освобождением поставщика УПАКОВАНного PST-хранилища, чтобы поставщик УПАКОВАНного PST-хранилища мог завершить работу должным образом. Функция завершает все объекты Session, связанные с поставщиком упакованного PST-хранилища. 
  
## <a name="cmsprovidershutdown-example"></a>Кмспровидер:: ShutDown () пример

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



[О примере поставщика упакованного PST-хранилища](about-the-sample-wrapped-pst-store-provider.md)
  
[Установка примера поставщика упакованного PST-хранилища](installing-the-sample-wrapped-pst-store-provider.md)
  
[Инициализация поставщика упакованного PST-хранилища](initializing-a-wrapped-pst-store-provider.md)
  
[Вход в систему поставщика упакованного PST-хранилища](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Использование поставщика упакованного PST-хранилища](using-a-wrapped-pst-store-provider.md)

