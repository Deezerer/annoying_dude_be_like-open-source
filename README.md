a .exe made in rust which repeats everything you say in cmd (no admin needed) with "annoyingdude:dude fr said" before,
press ctrl+c or type exitprogram to stop it
code: use std::io;

fn main() {
    println!("type and press enter, an annoying dude will repeat everything, ctrl+c or exitprogram to stop:");
    let mut input_string = String::new();

    while input_string.trim() != "exitprogram" {
        input_string.clear();
        io::stdin().read_line(&mut input_string).unwrap();
        println!("annoyingdude:dude fr said {}", input_string);
    }
    println!("exiting...");
}
