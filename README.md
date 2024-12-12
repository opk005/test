<?php
require 'inc/config.php';
require 'inc/head.php';
require 'inc/auth.php';

// Vérifier le rôle de l'utilisateur
if ($_SESSION['role'] !== 'Administrateur') {
    echo "Accès refusé. Seuls les administrateurs peuvent ajouter des fournisseurs.";
    exit();
}
