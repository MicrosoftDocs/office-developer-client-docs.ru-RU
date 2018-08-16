---
title: Завершение работы поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Последнее изменение: 2 июля 2012.'
ms.openlocfilehash: 5c8ad7443b0c1aa05f48284e4b09859ab53dd2c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812287"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Завершение работы поставщика упакованного PST-хранилища

 
  
**Относится к**: Outlook 
  
После завершения работы с оболочку поставщика хранилища личных папок (PST) файла, необходимо надлежащим образом завершение работы оболочку поставщика хранилища PST-файлов. Дополнительные сведения об использовании оболочку поставщика хранилища PST-файлов [с использованием поставщика оболочку хранения PST -файлов](using-a-wrapped-pst-store-provider.md)см.
  
Завершение работы оболочку поставщика хранилища PST-файлов, необходимо вызвать функцию **[IMSProvider::Shutdown](imsprovider-shutdown.md)** . Закрывает этой функции вниз оболочку поставщика хранилища PST определенным образом. 
  
В этом разделе демонстрируется функция **IMSProvider::Shutdown** с помощью пример кода из оболочку PST поставщик хранилища. В примере реализуется оболочку поставщика PST-файлов, который предназначен для использования совместно с использованием интерфейса API репликации. Дополнительные сведения о загрузке и установке оболочку PST поставщик хранилища [Оболочку PST поставщик хранилища](installing-the-sample-wrapped-pst-store-provider.md)см. Дополнительные сведения об API репликации можно [О репликации API](about-the-replication-api.md).
  
## <a name="shut-down-routine"></a>Завершение работы программы

Диспетчер очереди MAPI вызывает функцию **[IMSProvider::Shutdown](imsprovider-shutdown.md)** перед освобождает оболочку поставщика хранилища PST-файлов, чтобы оболочку поставщика хранилища PST-файлов можно завершить работу должным образом. Функция завершает работу всех объектов сеанса, связанных с переносами поставщика хранилища PST-файлов. 
  
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



[Сведения о примере поставщика упакованного PST-хранилища](about-the-sample-wrapped-pst-store-provider.md)
  
[Установка примера поставщика упакованного PST-хранилища](installing-the-sample-wrapped-pst-store-provider.md)
  
[Инициализация поставщика упакованного PST-хранилища](initializing-a-wrapped-pst-store-provider.md)
  
[Вход в систему поставщика упакованного PST-хранилища](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Использование поставщика упакованного PST-хранилища](using-a-wrapped-pst-store-provider.md)
