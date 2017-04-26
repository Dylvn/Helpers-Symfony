# Helpers-Symfony

## Doctrine2

- Add data to bdd example
```php
        $advert = new Advert();
        $advert->setTitle('Recherche Développeur Symfony');
        $advert->setAuthor('Dylan');
        $advert->setContent("Nous recherchons un développeur Symfony débutant sur Lyon.");

        // Création d'une image
        $image = new Image();
        $image->setUrl('http://sdz-upload.s3.amazonaws.com/prod/upload/job-de-reve.jpg');
        $image->setAlt('Job de rêve');

        // On lie l'image a une annonce
        $advert->setImage($image);

        // Création d'une premiére candidature
        $application1 = new Application();
        $application1->setAuthor('Marine');
        $application1->setContent("J'ai toutes les qualités requises");

        // Création d'une deuxiéme candidature
        $application2 = new Application();
        $application2->setAuthor('Pierre');
        $application2->setContent("Je suis super motivé.");

        // Je lie les candidatures à l'annonce
        $application1->setAdvert($advert);
        $application2->setAdvert($advert);
```
